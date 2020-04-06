---
layout: page
title: Bruce Chien
permalink: /about/
---
## Currently

SSD Firmware R&D Engineer.

## Employment

`2019 - `
__ESEC__ SSD 韌體工程師

`2016 - 2019` 
__[Quanta Storage Inc.][qsitw]__ SSD 韌體工程師

## Education

`2014 - 2016`
__國立臺灣師範大學__ 資訊工程學系 __碩士__

`2010 - 2014`
__國立臺灣海洋大學__ 資訊工程學系 __學士__

## Technical skills

* SSD: FTL, TCG
* Tool: Vim, Git
* C
* Embedded System (ARM)
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

[_github.com/Chienweichih/Voting-CAP_][Voting-CAP]
{: .right}

這是我的碩士論文，以 Java 實作 Socket 來模擬雲端儲存系統的環境。透過 Java 的 API 實作基於密碼學的通訊協定。使用者的客戶端不需要保留任何檔案的雜湊值，就能達到 proof of violation 和 real-time auditing。最終就是用這個專案得到各種實驗的數據，以證明本篇論文的可行性。

(這是一個用 Java 完成的 Project)
{: .right}

---

`No. 2`
__PD Protocol Parser__

[_github.com/Chienweichih/CCGX_PD_Parser_][PD_PARSER]
{: .right}

將 Cypress CY4500 EZ-PD™ Protocol Analyzer 錄出的 .ccgx files 另存成 csv 格式後，就可以利用這個工具來轉換成很容易閱讀的文件，不用再查詢 Spec 來比對 log 的意思。更重要的功能是，他可以為了不同的 VDM 來擴增不同的實作 (譬如 Display Port 或 HP 等 Vender 的 Alternate mode)。

(這是一個用 Python 完成的 Project)
{: .right}

---

`No. 3`
__PL2303 GPIO 工具__

[_github.com/Chienweichih/PL2303_GPIO_][PL2303_GPIO]
{: .right}

用 PL2303 USB to GPIO 晶片實作出的產測工具。控制 GPIO 開關 Type C cable 的 CC1, CC2 及 VBus，來做出 Type C cable 正反插的動作。這樣的工具不僅能夠省下人工插拔的動作，還能在接上電腦後自動判斷出接上的硬碟的名稱等等資訊，自動化很多需要判斷的項目。

(這是由官網提供的 [MFC Project][oneping] 改寫的一個 command line tool)
{: .right}

---

`No. 4`
__熱門景點的臉書打卡數與天氣指數的關係之研究__

[_github.com/Chienweichih/TPWeather_][TPWeather]
{: .right}

本研究要探討地區性人氣活躍程度，是否和社群網站的打卡數量以及天氣的因素有所關連。我們利用 Facebook 的 API 取得景點的打卡數量、利用 Python 撰寫爬蟲程式抓取台北市國小的氣象資料。以迴歸分析計算出的數學模型觀察這些資料之間的關聯，進而估測出特定景點的 Point of Interest (POI) 值。

(這是一個用 Python 實作的 Web Scraping Project)
{: .right}

---

`No. 5`
__二維條碼文件證書認證系統__

[_github.com/Chienweichih/MyUndergraduateProject_][MyUndergraduateProject]
{: .right}

這是我的大學畢業專題，目標是讓紙本文件也能夠利用密碼學的方法來保證資料的完整性。所以我們在 Server 端保存文件內容的數位簽章，使用者端的應用程式可以驗證文件內容是否和 Server 上的資料相符。為了增加紙本文件和數位資料的連結，我們使用 QR-Code 的技術，將 QR-Code 條碼印刷在紙本文件上。使用者端掃描條碼後便能輕鬆地完成認證。

(這是一個結合 Java 實作後端程式及 Android 介面的一個 Project)
{: .right}

[qsitw]: http://www.qsitw.com/page/tw/index.html
[masters_thesis]: http://handle.ncl.edu.tw/11296/ndltd/10270759124789943046
[Voting-CAP]: https://github.com/Chienweichih/Voting-CAP
[PD_PARSER]: https://github.com/Chienweichih/CCGX_PD_Parser
[PL2303_GPIO]: https://github.com/Chienweichih/PL2303_GPIO
[oneping]: http://www.oneping.com.tw/fileDownload.htm
[TPWeather]: https://github.com/Chienweichih/TPWeather
[MyUndergraduateProject]: https://github.com/Chienweichih/MyUndergraduateProject
