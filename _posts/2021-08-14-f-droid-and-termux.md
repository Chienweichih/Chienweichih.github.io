---
layout: post
title: "我的 F-Droid 和 Termux 程式整理"
date: 2021-8-15 00:40:00 +0800
tags: [FOSS, Android]
comments: true
share: true
---

最近在研究 F-Droid 上的 FOSS app，來記錄一下找了哪些好東西。

# FOSS APP on F-Droid

### 連線
GadgetBridge
: 連接小米手環，同步資料 [*nodomain.freeyourgadget.gadgetbridge*]

OpenTracks
: 運動紀錄，匯出 kmz 檔可以在 Organicmaps 開啟 [*de.dennisguse.opentracks*]

Port Authority
: 搜尋同一個 wifi 下的裝置 [*com.aaronjwood.portauthority*]

Rtl-sdr driver
: 我用來聽 FM 的 dongle 的 driver [*marto.rtl_tcp_andro*]

ScreenStream
: 透過 wifi 投放手機畫面，像 ChromeCast 的功能 [*info.dvkr.screenstream*]

WiFiScanner
: 搜尋 wifi 訊號 [*org.bitbatzen.wlanscanner*]

### 遊戲
DartChecker
: 飛鏢記分板 [*com.DartChecker*]

Freebloks
: Blokus 角鬥士棋 [*de.saschahlusiak.freebloks*]

RetroArch
: 電玩模擬器，要新增這個 repo 才能下載 (https://fdroid.libretro.com) [*com.retroarch.aarch64*]

Sokoban(g)
: Sokoban 倉庫番 [*dev.obfusk.sokobang*]

SuperTuxKart
: 賽車遊戲 [*org.supertuxkart.stk*]

### 網路
Blokada 5
: 擋廣告工具 [*org.blokada.fem.fdroid*]

FairEmail
: 電子信箱，但是要到 Play 商店下載的版本才能支援 OAuth 登入 [*eu.faircode.email*]

Fennec
: Firefox 網頁瀏覽器 [*org.mozilla.fennec_fdroid*]

Frost for Facebook
: Facebook 瀏覽器 [*com.pitchedapps.frost*]

Infinity
: Reddit 瀏覽器 [*ml.docilealligator.infinityforreddit*]

### 多媒體
AntennaPod
: 聽 PodCast [*de.danoeh.antennapod*]

Binary Eye
: QRCode 條碼掃描器 [*de.markusfisch.android.binaryeye*]

Microphone
: 讓麥克風的聲音從耳機輸出 [*net.bitplane.android.microphone*]

NewPipe
: YouTube 瀏覽器 (無廣告，免登入) [*org.schabi.newpipe*]

Tachiyomi
: 看漫畫 [*eu.kanade.tachiyomi*]

Tuner
: 調音器 [*org.billthefarmer.tuner*]

VLC
: 影音播放器 [*org.videolan.vlc*]

### 閱讀
Aard 2
: 離線字典，WordNet 和 FreeDict 很棒 [*itkach.aard2*]

Feeder
: RSS 閱讀器 [*com.nononsenseapps.feeder*]

MuPDF
: 文件閱讀器，可以開 pdf, mobi, epub, cbz 等格式 [*com.artifex.mupdf.viewer.app*]

Nihonoari
: 練習日文假名 [*com.LAPARCELA.nihonoari*]

Print
: 把網頁或文字轉成 pdf 檔 [*org.billthefarmer.print*]

### 科學與教育
Organicmaps
: 使用 OpenStreetMap 的離線地圖，maps.me 的替代方案 (更好) [*app.organicmaps*]

QuickWeather
: 使用 OpenWeatherMap 的天氣資訊 [*com.ominous.quickweather*]

Sky Map
: 星空圖 [*com.google.android.stardroid*]

UnicodePad
: 可以查 Unicode 編碼 [*jp.ddo.hotmist.unicodepad*]

### 系統
Coffee
: 讓螢幕 Always On [*com.github.muellerma.coffee*]

F-Droid
: FOSS APP Repository [*org.fdroid.fdroid*]

Muzei
: 手機桌布 [*net.nurik.roman.muzei*]

Olauncher
: 極簡風格啟動器 (桌面) [*app.olauncher*]

Termux
: 終端模擬器 [*com.termux*]

---

終於寫完我最近找到的 F-Droid APP 了，接下來列一下我在 Termux 上安裝了什麼應用。

# Package on Termux

這些是可以直接用 pkg install 的 package

* [bash-completion](https://github.com/scop/bash-completion)
* [bc](https://www.gnu.org/software/bc/)
* [clang](https://clang.llvm.org/)
* [cmatrix](https://github.com/abishekvashok/cmatrix)
* [ffmpeg](https://www.ffmpeg.org/)
* [figlet](http://www.figlet.org/)
* [fzf](https://github.com/junegunn/fzf)
* [git](https://git-scm.com/)
* [greed](https://gitlab.com/esr/greed)
* [make](https://www.gnu.org/software/make/)
* [ncurses-utils](https://invisible-island.net/ncurses/)
* [neofetch](https://github.com/dylanaraps/neofetch)
* [openssh](https://www.openssh.com/)
* [perl](https://www.perl.org/)
* [ranger](https://github.com/ranger/ranger)
* [ripgrep](https://github.com/BurntSushi/ripgrep)
* [tig](https://github.com/jonas/tig)
* [tty-clock](https://github.com/xorg62/tty-clock)
* [vim](https://www.vim.org/)
* [wget](https://www.gnu.org/software/wget/)

還有一些要手動下載、編譯的工具：

* [ccal](https://github.com/liangqi/ccal)
* [ctags](http://ctags.sourceforge.net/)
* [freecell](https://www.linusakesson.net/software/freecell.php)
* [nihonoari](https://github.com/aeri/Nihonoari)
* [programmer-calculator](https://github.com/alt-romes/programmer-calculator)
* [tetris](https://github.com/jserv/tetris)
* [youtube-dl](https://github.com/ytdl-org/youtube-dl)

再搭配我的 dotfiles 設定環境

[https://github.com/Chienweichih/dotfiles](https://github.com/Chienweichih/dotfiles)

這樣就可以把常用的工具都裝好了! 其實這些程式在[之前的文章](https://chienweichih.github.io/tinker-board-s-software/)有介紹過，這裡再整理一次。

如果要讓 Termux 可以讀寫手機的儲存空間，記得下這個 command:

> [termux-setup-storage](https://wiki.termux.com/wiki/Termux-setup-storage)

