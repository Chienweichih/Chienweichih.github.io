---
layout: page
title: 簡偉智 - Bruce Chien
permalink: /about/
---
## Currently

[Quanta Storage Inc.][qsitw] Consumer Electronics Firmware R&D Engineer.

## Employment

`2016-2018` 
__Quanta Storage Inc.__ [SSD][Techman] 韌體工程師

`2018-` 
__Quanta Storage Inc.__ 消費性電子 韌體工程師

## Education

`2014-16`
__國立臺灣師範大學__ 資訊工程學系碩士

`2010-14`
__國立臺灣海洋大學__ 資訊工程學系學士

## Technical skills

* Git
* C
* Embedded System (ARM)
* Flash Translation Layer in SSD
* USB Type-C, Power Delivery
* Python
* Java, C#, MFC
* Linux

## Master's thesis

__利用備份與投票技術實作雲端儲存之即時行為違反證明技術__

*Implementing Real-time POV for Cloud Storage by Replication and Voting*
{: .right}

In this paper we study how to develop an efficient real-time auditing and proof of violation on cloud storage. Proof of violation can let user and service provider generate cryptographic proofs that used to proof service provider’s properties violate, or let service provider proof it’s innocence. Proof of violation are solutions for obtain mutual nonrepudiation between user and service provider. Real-time auditing perform on the end of every file operation so that the violation of the service provider can be found instantly. Existing solutions need to cache file’s hash value on client device. Storing and synchronize these file’s hash value are really huge overhead for client device. If a client device being offline in ages, synchronize to latest file’s hash value will speed a really long time.  
We propose a real-time proof of violation for cloud storage by replication and voting that let client device don’t need to cache any file’s hash value. Using multiple Independent service provider so that client device can real-time audit, support proof of violation, and having multiple file replication. Experimental results are presented that our scheme outperforms previous work 8 times by average, and in the worst case our scheme outperforms previous work by 20 times. Service providers of cloud storage can use the propose scheme to provide a mutual nonrepudiation guarantee in their service-level agreements.

__Link: [http://handle.ncl.edu.tw/11296/ndltd/10270759124789943046][masters_thesis]__
{: .center}

## Projects

`No. 1`
__利用備份與投票技術實作雲端儲存之即時行為違反證明技術__

[_github.com/CloudComLab/Voting-CAP_][Voting-CAP]
{: .right}

我的碩士論文，一個有效率的即時稽核技術以及雲端儲存系統使用的違反證明技術。我們提出一個投票的方法讓客戶端的設備不需要保留任何的檔案的雜湊值。利用多個獨立的服務提供者，客戶端不僅能即時的稽核、支援 POV 技術，又能同時擁有多份的備份。實驗利用 Java 密碼學的 api 、以 Socket 實作網路資訊傳輸等等，來模擬雲端儲存系統的操作。

(使用語言：Java)
{: .right}

---

`No. 2`
__CarTrace App__

專案名稱為 CarTrace App，目的是要開發一個可以連線至車機手機程式，有讀取QR code註冊帳號，接收Server的回傳資料，回報問題給Server，管理車機傳送的照片等等功能之應用程式。我和實驗室的同學合作，以Github管理我們的專案。我所撰寫的功能有：註冊頁面的介面，利用手機照相機讀取QR code的功能，可以滑動翻閱的相簿和通知等功能。

(使用語言：Java - Android)
{: .right}

---

`No. 3`
__熱門景點的臉書打卡數與天氣指數的關係之研究__

[_github.com/Chienweichih/TPWeather_][TPWeather]
{: .right}

透過打卡的數量，以及天氣的指數，探討兩者間的相關性造成地區性的影響人氣活耀程度的關聯因素,並且以迴歸分析方法計算能夠表示關聯因素的數學模型進而可以估測特定景點的 Point of Interest(POI)值，提供給景點拜訪者所參考。其中利用 Python 撰寫爬蟲程式，抓取台北市國小的氣象資料。

(使用語言：Python)
{: .right}

---

`No. 4`
__生物資訊文件分析__

[_github.com/Chienweichih/BioInfo_Project_][BioInfo_Project]
{: .right}

從 BioPortal 的 Gene Ontology 資料庫得到的資料，讓使用者可以 query 或是分析一篇論文的摘要，並利用 Django 寫成一個網站。

(使用語言：Python - Django)
{: .right}

---

`No. 5`
__二維條碼文件證書認證系統__

[_github.com/Chienweichih/MyUndergraduateProject_][MyUndergraduateProject]
{: .right}

這是我的大學畢業專題。本專題運用QR-code儲存資料量多且讀取便利、不易失真的特性， 設計以Android手機讀取紙本文件上存於QR-code中的數位資料，使用者可以運用手機即時驗證文件中：時戳資料、簽章資料及文件內容的正確性，如此可以透過傳統紙本文件平行傳遞可驗證的數位資料，強化紙本文件的功能。

(使用語言：Java, Java - Android)
{: .right}

[qsitw]: http://www.qsitw.com/page/tw/index.html
[Techman]: http://tm-ssd.com/
[masters_thesis]: http://handle.ncl.edu.tw/11296/ndltd/10270759124789943046
[Voting-CAP]: https://github.com/CloudComLab/Voting-CAP
[TPWeather]: https://github.com/Chienweichih/TPWeather
[BioInfo_Project]: https://github.com/Chienweichih/BioInfo_Project
[MyUndergraduateProject]: https://github.com/Chienweichih/MyUndergraduateProject
