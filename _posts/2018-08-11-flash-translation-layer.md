---
layout: post
title: "Flash Translation Layer (FTL)"
date: 2018-11-04 21:20:00 +0800
tags: [SSD, FTL]
comments: true
share: true
---

這篇文章是要整理我這兩年來做的工作，SSD裡的Flash Translation Layer (FTL)。

FTL是介於SSD前端和後端之間的一個轉換層，前端指的是和Host用Protocol溝通的那邊，後端是真正儲存資料的實體的Nand Flash這邊。以前傳統的Hard Disk可以直接從Host指定把資料存在硬碟裡的任何區域，為什麼SSD還要中間多一層FTL呢?這就是傳統硬碟和固態硬碟不同之處，和固態硬碟使用的Nand Flash特性有關。

使用Nand Flash有幾個規則：<br />
1. 必須先Erase，才能Program。寫入之前要先抹除，沒有抹除而直接複寫的話資料會壞掉讀不出來。而且抹除的時間 >> 寫入的時間 >> 讀取的時間。
2. 抹除和讀寫的單位不一樣，抹除的最小單位是一個Block，讀寫的最小單位是一個Page，一個Block大約是64個Page(或更多)。
3. Nand Flash是有壽命的，他的壽命可以用Block的PE Cycle (Program/Erase Cycle)來計算，SLC大概50K次、MLC大概3K次、TLC小於1K次，使用超過這些次數不一定真的會壞掉，但是有很高的機率資料會越來越難讀出來。
4. 資料存進去後，若只一直讀取而不再抹除重寫，周圍的Page裡面儲存的電子(代表0和1的bits)會被讀取的電壓所影響，而造成資料錯誤。
5. 還有好多特性，像TLC有很多奇奇怪怪的事情會發生，太久沒讀資料會不見之類的，就不繼續寫下去了，因為我也不是專業研究Nand Flash的。

列了這幾個特性，就可以開始說為什麼SSD裡需要FTL了。

當然，你可以把Nand Flash當作傳統硬碟一樣來實作，寫入前先抹除，然後把你要寫的資料寫到指定的位子，OK。<br />
然後要修改同一個位子的值，好，那就先把他抹除，然後寫入新的資料。<br />
但是如果這個Block上其他的Page已經有先前的資料，那就被抹除掉了，所以在抹除之前，要把資料全部備份到其他位子，Nand Flash或Ram之類的，然後才可以抹除、再寫回去，經過那麼多步驟終於更新好一筆資料了。<br />
以上的步驟不只很冗長，而且你的SSD一下子就會死掉了。寫個幾千筆資料Nand Flash就壞光光，你的產品只能保固1個月，這樣好像不太對。<br />
為了更新一個Page的資料，要犧牲其他64個Page陪你重寫，增加PE Cycle、沒效率又速度慢。<br />
所以該FTL上場了。首先，FTL需要一個Table，這也是FTL最重要的工作：L2P Table (Logical page number to Physical page number Table)。<br />
L2P Table紀錄虛擬和實體的Page Number之間的轉換。所謂虛擬的Page Number(LPN)就是Host以為他的資料存的地址，實體的Page Number(PPN)是真正寫到實體Nand Flash的地址。舉個例子：

1. Host把資料寫到地址0x123，實體寫到位置0x123，L2P上記錄 0x123 -> 0x123。
2. Host修改位子0x123的資料。這時如果直接修改實體位置0x123，會陪葬其他的Page。所以我們把資料寫到另一個地址，0x124，L2P改成0x123 -> 0x124，然後把0x123紀錄為invaild(另一個FTL的Table)。
3. Host想讀0x123的資料，FTL就先去L2P查，看到了0x123 -> 0x124，於是就去Nand Flash的0x124位子把資料傳出來給Host。

所以更新資料的動作變成把新的資料放到其他地址，然後再更改L2P Table。因為少了很多抹除的動作，速度比之前的方法快很多很多，壽命也延長了，真是可喜可賀。

但是你以為就這樣結束了嗎，不，問題越來越多啦：<br />
1. 為了速度，L2P是記在Ram上。只要一斷電，L2P不見，你的SSD就等於是Reset了。(也有人在研究不把L2P存在Ram，改存在Nand Flash上但又能維持速度，不過這裡不討論這個)
2. 一直寫入新的資料到其他位子，舊的資料設成invalid，但是一顆SSD上的Nand Flash是有限的呀，總有一天會用到全部都是invalid，該怎麼辦呢。

第一個問題，有一種暴力解法，就是在重新上電時去讀取Nand Flash上所有的Page。全部掃一次知道了哪些Page是vaild、哪些是invalid，然後再把L2P Table全部重建起來。太好了過了半個小時終於開機了，疑，好像哪裡怪怪的。<br />
這裡我提供一個方法：就是每隔一段時間，或是每寫了多少的資料，就把L2P Table寫入Nand Flash裡。這樣在重新上電時，你可以基於最近的一份L2P Table來重建斷電前最後的狀態，那可以減少很多讀取的時間，也降低資料大量遺失的機率。但是這畢竟是額外的工作，會降低整個SSD的讀寫速度(IOPS之類的)，而且也會浪費Nand Flash的使用空間。當然電腦科學是一直在進步，不斷有人提出新的方法來管理L2P的問題，一定有越來越厲害的方法會出現的。

第二個問題的解決方法，就是大家可能常常聽到的Garbage Collection (GC)。既然一堆Block都是invalid了，那我們就來整理，全部都是invalid page的Block就直接Erase掉拿來使用呀，酒矸倘賣無。阿，那如果Host故意每個Block都留一個valid的資料，那要怎麼辦。所以我們要在還有可以用的Block的時候，把那些invalid比較多的Block的資料搬到空的Block上，也就是內部自己再重寫一次資料，再把原本的page設成invalid。全部整理完以後，就又有很多Block可以Erase了，那可以用的Block的數量就會漸漸恢復。

雖然解決了問題，但是也消耗了很多資源。多餘的內部的寫入不是Host想要的，會減慢硬碟讀寫的速度，會減少Nand Flash的壽命，還會讓連續的資料變得不連續(當然這也是減慢讀取的時間)。所以事有利弊，既然有天生的缺陷就很難找到完美的作法，只能找到效率與壽命的平衡點，讓這顆固態硬碟能夠活出完美的人生，就是大家所期盼的結局。(我到底再寫什麼)

一定還有很多東西可以寫的，但是以這個網站的更新速度...有緣再繼續吧。很開心終於簡單的整理完我這兩年做的工作的內容了，期許未來不管做什麼都能記得剛畢業時的理想，繼續進步下去

謹以此文紀念小明SSD部門<br />
![NP-Solution-II]({{ site.baseurl }}/images/2018-08-11-flash-translation-layer/NP-Solution-II.jpg){: .center-image}
