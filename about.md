---
layout: page
title: Bruce Chien
permalink: /about/
---
## Employment

`2019 - 2025`
__[YEESTOR Microelectronics Co., Ltd][yeestor]__ SSD 韌體工程師

`2016 - 2019` 
__[Quanta Storage Inc.][qsitw]__ SSD 韌體工程師

## Education

`2014 - 2016`
__國立臺灣師範大學__ 資訊工程學系 __碩士__

`2010 - 2014`
__國立臺灣海洋大學__ 資訊工程學系 __學士__

## Experience

就學期間學習了多種程式語言基礎、資料結構演算法、計算機架構組織，後來對資訊安全深感興趣，進修密碼學相關課程，大學和研究所的專題研究都是和 Security 相關的題目。

大學專題是用 Java 實作紙本文件的簽章認證系統，除了密碼學的簽章加密、還用到了 QR-Code 的編碼解碼功能實作。研究所論文題目為《利用備份與投票技術實作雲端儲存之即時行為違反證明技術》，這是透過類似 Blockchain 的概念將文件系統做出經 Service provider 認證的簽章，用於雲端儲存系統的 Real-time auditing.

畢業後找到的第一份工作就和 Storage 相關，在廣明光電開始 FTL FW 的任務。當時是用 Marvell 的 Controller，主要是 "Eldora"，維護 L2P、Block 的管理、GC、Snapshot、POR 和 SPOR 的上電恢復流程處理、Trim、Sanitize 等 admin cmd 的 FW，新增功能修改 bug 等等。後來公司因業務調整把 SSD 部門解散，趁這個機會我換到了消費性電子的部門，在這裡做了 Type-C 產品的 FW （PD協定）、MFC 寫的 MPTool 等功能。

後來來到了大心電子，也就是現在的得一微電子。當時公司想要做 TCG OPAL 的功能，於是請我去支援，我和另一位資深的同事從無到有的把 TCG Pyrite 和 TCG OPAL 的功能實作出來，把相關的 Spec 都看了，後來的成果是有通過 Ulink Drive Master 認證的。接著就是 System FW 的相關 FW 處理、新增功能、處理各類問題。有經歷過阿里主導的一個 10 cores CPU 的 enterprise FW 的開發，前期主要是在仿真系統上做出了讀寫、GC、斷電上電正常的 System FW。後來也去支援了 dramless 的案子、工控產品的案子，發了很多 FW 版本，解決客訴問題等等。

從畢業到現在主要都是 SSD FW 的經歷，8 年半的工作經歷我學習到各式各樣的經驗。除了工作中需要的 System FW、TCG OPAL 等專業外，我也自己學習精通 Git 和 Vim 等等工具，熟悉 Linux command line 的使用。對技術的學習始終抱持著一顆充滿興趣的心，任勞任怨的完成一切交辦的任務。

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

將 Cypress CY4500 EZ-PD™ Protocol Analyzer 錄出的 .ccgx files 另存為 csv 格式後，便可以透過這個工具轉換出容易閱讀的文件，不需要再麻煩的查詢 Spec 來比對 log 的意思。還可以替不同的 VDM 實作他們所需要的功能 (例如 Display Port，或是 HP 等等 Vender 的 Alternate mode)。

(這是一個用 Python 完成的 Project)
{: .right}

---

`No. 2`
__PL2303 GPIO 工具__

[_https://github.com/Chienweichih/PL2303_GPIO_][PL2303_GPIO]
{: .right}

使用 PL2303 USB to GPIO 晶片實作出的產測工具。透過對 GPIO 的操作，控制 Type-C cable 的 CC1, CC2 及 VBus 開關，來做出 Type-C cable 正反插的動作。這個工具不僅能夠省下人力來插拔 DUT，也能在接上電腦後自動判斷出硬碟的名稱等等資訊，用於自動化處理相關流程。

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

這是我的碩士論文，以 Java 實作 Socket 來模擬雲端儲存系統的環境。透過 Java 的 API 實作基於密碼學的通訊協定。使用者的客戶端不需要保留任何檔案的雜湊值，就能達到 proof of violation 和 real-time auditing。最終利用這個專案得到各種實驗的數據，以證明本篇論文的可行性。

(這是一個用 Java 完成的 Project)
{: .right}

---

`No. 5`
__二維條碼文件證書認證系統__

[_https://github.com/Chienweichih/MyBachelorProject_][MyBachelorProject]
{: .right}

這是我的大學畢業專題。紙本文件可能會有被偽造修改的風險，如果能透過密碼學的簽章，就可以保護資料的完整性。實作的方法是在 Server 保存文件內容的數位簽章，使用者透過手機的應用程式便能驗證文件內容是否和 Server 上的資料相符。為了讓紙本文件和數位資料能夠產生關聯，我們使用 QR-Code 的技術，將 QR-Code 條碼印刷在紙本文件上。使用者掃描條碼後便能快速的完成認證。

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
