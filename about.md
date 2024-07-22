---
layout: page
title: Bruce Chien
permalink: /about/
---
## Employment

`2019 -   `
__[YEESTOR Microelectronics Co., Ltd][yeestor]__ SSD 韌體工程師

`2016 - 2019` 
__[Quanta Storage Inc.][qsitw]__ SSD 韌體工程師

## Education

`2014 - 2016`
__國立臺灣師範大學__ 資訊工程學系 __碩士__

`2010 - 2014`
__國立臺灣海洋大學__ 資訊工程學系 __學士__

## Experience

我是海洋大學資工系畢業，師範大學資工所畢業，大學和研究所都是研究 Security 相關的題目，有興趣的話可以看一下後面的附件。

畢業之後到廣明光電上班，寫 FTL 相關的 FW，就是 L2P、Block 的管理、GC、Snapshot、POR 和 SPOR 的上電恢復流程處理、Trim、Sanitize 等 admin cmd。在廣明做了 3 年，後來因為部門倒了所以就換公司了，在廣明最後的半年還有去接觸了一下消費性電子的 FW，做了 Type-C 相關的產品。

再來去了大心電子，公司後來被併購所以現在是得一微電子。剛到這家公司的時候他們請我去支援做 TCG 的 FW，當時我們就兩個人從無到有的把 TCG Pyrite 和 TCG OPAL 的功能實做出來，是有通過 Ulink Drive Master 認證的。後來就是做 FTL、Read、Write、Throttle 相關的 FW。有做過阿里開的 10核 CPU enterprise 的 FW，有做過 dramless FTL 的 FW，有做過工控的 FW，目前的公司經歷 5 年半，做 SSD FW 的經歷已經超過 8 年。

我熱愛學習，精通 Git 和 Vim 工具的使用，熟悉 linux cmd line，會寫 C、Python、Java、Shell Script，專長如前面所說的是 SSD 的 FTL、Read、Write、TCG、Security。

## Technical skills

* C
* SSD: FTL, TCG
* Tool: Vim, Git
* Linux command line
* Python, Java, Shell Script
* Cryptography
* Embedded System (ARM)
* USB Type-C, Power Delivery

## Projects

`No. 1`
__PD Protocol Parser__

[_https://github.com/Chienweichih/CCGX_PD_Parser_][PD_PARSER]
{: .right}

將 Cypress CY4500 EZ-PD™ Protocol Analyzer 錄出的 .ccgx files 另存成 csv 格式後，就可以利用這個工具來轉換成很容易閱讀的文件，不用再查詢 Spec 來比對 log 的意思。更重要的功能是，他可以為了不同的 VDM 來擴增不同的實作 (譬如 Display Port 或 HP 等 Vender 的 Alternate mode)。

(這是一個用 Python 完成的 Project)
{: .right}

---

`No. 2`
__PL2303 GPIO 工具__

[_https://github.com/Chienweichih/PL2303_GPIO_][PL2303_GPIO]
{: .right}

用 PL2303 USB to GPIO 晶片實作出的產測工具。控制 GPIO 開關 Type C cable 的 CC1, CC2 及 VBus，來做出 Type C cable 正反插的動作。這樣的工具不僅能夠省下人工插拔的動作，還能在接上電腦後自動判斷出接上的硬碟的名稱等等資訊，自動化很多需要判斷的項目。

(這是由官網提供的 [MFC Project][oneping] 改寫的一個 command line tool)
{: .right}

---

`No. 3`
__熱門景點的臉書打卡數與天氣指數的關係之研究__

[_https://github.com/Chienweichih/TPWeather_][TPWeather]
{: .right}

本研究要探討地區性人氣活躍程度，是否和社群網站的打卡數量以及天氣的因素有所關連。我們利用 Facebook 的 API 取得景點的打卡數量、利用 Python 撰寫爬蟲程式抓取台北市國小的氣象資料。以迴歸分析計算出的數學模型觀察這些資料之間的關聯，進而估測出特定景點的 Point of Interest (POI) 值。

(這是一個用 Python 實作的 Web Scraping Project)
{: .right}

---

`No. 4`
__利用備份與投票技術實作雲端儲存之即時行為違反證明技術__

*Implementing Real-time POV for Cloud Storage by Replication and Voting*
{: .right}

In this paper we study how to develop an efficient real-time auditing and proof of violation on cloud storage. Proof of violation can let user and service provider generate cryptographic proofs that used to proof service provider’s properties violate, or let service provider proof it’s innocence. Proof of violation are solutions for obtain mutual nonrepudiation between user and service provider. Real-time auditing perform on the end of every file operation so that the violation of the service provider can be found instantly. Existing solutions need to cache file’s hash value on client device. Storing and synchronize these file’s hash value are really huge overhead for client device. If a client device being offline in ages, synchronize to latest file’s hash value will speed a really long time.  
We propose a real-time proof of violation for cloud storage by replication and voting that let client device don’t need to cache any file’s hash value. Using multiple Independent service provider so that client device can real-time audit, support proof of violation, and having multiple file replication. Experimental results are presented that our scheme outperforms previous work 8 times by average, and in the worst case our scheme outperforms previous work by 20 times. Service providers of cloud storage can use the propose scheme to provide a mutual nonrepudiation guarantee in their service-level agreements.

__Link: [https://hdl.handle.net/11296/8ub4ku][masters_thesis]__
{: .center}

[_https://github.com/Chienweichih/Voting-CAP_][Voting-CAP]
{: .right}

這是我的碩士論文，以 Java 實作 Socket 來模擬雲端儲存系統的環境。透過 Java 的 API 實作基於密碼學的通訊協定。使用者的客戶端不需要保留任何檔案的雜湊值，就能達到 proof of violation 和 real-time auditing。最終就是用這個專案得到各種實驗的數據，以證明本篇論文的可行性。

(這是一個用 Java 完成的 Project)
{: .right}

---

`No. 5`
__二維條碼文件證書認證系統__

[_https://github.com/Chienweichih/MyBachelorProject_][MyBachelorProject]
{: .right}

這是我的大學畢業專題，目標是讓紙本文件也能夠利用密碼學的方法來保證資料的完整性。所以我們在 Server 端保存文件內容的數位簽章，使用者端的應用程式可以驗證文件內容是否和 Server 上的資料相符。為了增加紙本文件和數位資料的連結，我們使用 QR-Code 的技術，將 QR-Code 條碼印刷在紙本文件上。使用者端掃描條碼後便能輕鬆地完成認證。

(這是一個結合 Java 實作後端程式及 Android 介面的一個 Project)
{: .right}



[yeestor]: https://www.104.com.tw/company/1a2x6bkpa1
[qsitw]: https://www.104.com.tw/company/7qfuky8
[PD_PARSER]: https://github.com/Chienweichih/CCGX_PD_Parser
[PL2303_GPIO]: https://github.com/Chienweichih/PL2303_GPIO
[oneping]: http://www.oneping.com.tw/fileDownload.htm
[TPWeather]: https://github.com/Chienweichih/TPWeather
[masters_thesis]: https://hdl.handle.net/11296/8ub4ku
[Voting-CAP]: https://github.com/Chienweichih/Voting-CAP
[MyBachelorProject]: https://github.com/Chienweichih/MyBachelorProject
