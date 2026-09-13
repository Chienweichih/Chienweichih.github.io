---
permalink: /about/
title: About
---

# Bruce Chien
Senior SSD Firmware Engineer

📧 email@example.com ｜ 📍 Taipei, Taiwan ｜ 📞 0000-000-000

## About
10 年 SSD 韌體開發經驗，橫跨消費級與企業級產品線，專精 Flash Translation Layer (FTL)、TCG Opal 安全功能實作，以及 NVMe/PCIe 協定除錯。

## Experience

### 專案副主任 — [宇瞻科技]
*Mar. 2025 – Present*
- ...

### 資深工程師 — [得一微電子]（原 [大心電子]，2020年併購）
*Apr. 2020 – Feb. 2025*
- 在阿里設計的 10 Cores Controller，實作流控、WL、PLP 斷電上電的 System FW
- 合作實作 dramless 三級 L2P Table 的功能，能支援到 2TB 容量
- 在得一工控產品的案子，實作客戶想要的 vendor cmd，打包版本，解決客訴問題

### 高級工程師 — [大心電子]
*Mar. 2019 – Apr. 2020*
- 與資深工程師協作，從無到有完整實作 TCG Opal 安全功能，負責 `Next`、`Authenticate`、`Activate` 等核心 method 邏輯開發
- 依照 spec 規範實作 Single User Mode、Block SID 等 feature set，包含對應 table 與 method 開發
- 使用 ULINK DriveMaster 進行功能驗證測試，並針對測試中發現的問題進行除錯與修正
- 完成之韌體通過驗證並交付客戶
- 實作 dram base 的 memory remap 功能，修改 Register 控制流程，可以支援到 8GB

### 工程師 — [廣明光電]
*Aug. 2016 – Feb. 2019*
- 負責 Marvell Eldora 的 FTL FW
- 實作 Erase Fail Markbad 的流程處理
- 在消費性電子部門，負責 Type-C 產品 Cypress PD controller 的 FW

## Skills
- **語言**：C, Python, Shell Script
- **領域知識**：FTL, TCG Opal
- **協定**：NVMe, PCIe, SATA, USB Type-C, Power Delivery
- **工具**：JTAG, ULINK DriveMaster, Git, Linux CLI, Vim

## Projects
- **[Sedutil 測試腳本](https://github.com/Chienweichih/sedutil)** - 修改 sedutil 程式和編寫測試腳本
- **[TCG OPAL Parser](https://github.com/Chienweichih/TCG_OPAL_SimParser)** - This project is a parser for TCG Opal packets 
- **[PD Protocol Parser](https://github.com/Chienweichih/CCGX_PD_Parser)** — 將 Analyzer 錄出的檔案轉換為容易閱讀的文件，不需要再麻煩的查詢 Spec 來比對 log 的意思
- **[PL2303 GPIO 工具](https://github.com/Chienweichih/PL2303_GPIO)** — 透過對 GPIO 的操作，控制 Type-C cable 的 CC1, CC2 及 VBus 開關，來做出 Type-C cable 正反插的動作
- **[利用備份與投票技術實作雲端儲存之即時行為違反證明技術](https://github.com/Chienweichih/Voting-CAP)** — 我的碩士論文的實作，以 Java 實作 Socket 來模擬雲端儲存系統的環境，透過 Java 的 API 實作基於密碼學的通訊協定
- **[熱門景點的臉書打卡數與天氣指數的關係之研究](https://github.com/Chienweichih/TPWeather)** — 利用 Facebook 的 API 取得景點的打卡數量、利用 Python 撰寫爬蟲程式抓取台北市國小的氣象資料
- **[二維條碼文件證書認證系統](https://github.com/Chienweichih/MyBachelorProject)** — 我的大學畢業專題的實作，在 Server 保存文件內容的數位簽章，透過手機的驗證文件內容

## Education
國立臺灣師範大學 資訊工程碩士，2016
國立臺灣海洋大學 資訊工程學士，2014

<div style="break-after:page"></div>
