---
layout: post
title: "Tinker Board Debian OS 應用整理"
date: 2020-12-10 15:30:00 +0800
tags: [Tinker Board, Debian]
comments: true
share: true
---

最近在玩 [Asus Tinker Board S][Tinker-Board-S]。一開始是看上他的 24-bit/192kHz 音訊輸出，不用再加 DAC HAT 就能聽高音質的音樂，沒想到除了聽音樂以外還有很多好用的應用。

[Volumio][volumio] 聽音樂、[Lakka][lakka] 玩遊戲、[LibreELEC][libreelec] 看影片、[Android][TinkerBoardOS] 拿來看漫畫，或是各種 Android 能做的事，都很好用。

以上的系統安裝都很簡單，把映像檔燒到 SD 卡再簡單設定一下就可以用了。

---

接下來是 [Tinker Board Debian OS][TinkerBoardOS] 的整理

系統安裝好之後，我做了這些設定：

1. 把 locale 改成 Chinese zh UTF-8，把字體改成 IPAPGothic 和 DejaVu Sans Mono 看起來比較順眼。
2. 安裝 hime (中文輸入法), im-config (輸入法切換), hime-anthy (日文輸入)。  
   用 `$im-config -n hime` 設定。
3. 照我之前寫的 [dotfiles][dotfiles] 來設定 Git 和 Vim。
4. 安裝 ffmpeg (編輯影片工具)。
5. 安裝 mupdf (PDF viewer)。
6. 安裝 vlc (影片播放器)。
7. 安裝 firefox-esr (網頁瀏覽器)。
8. 安裝 libreoffice (Office 軟體)。
9. 安裝幾個實用的工具，需要從 source build：

    * [tig][tig]: Text-mode interface for git
    * [youtube-dl][youtube-dl]: Command-line program to download videos from YouTube.com and other video sites
    * [ccal][ccal]: Chinese Calendar
    * [freecell][freecell]: This is a console (ncurses) version of the popular and addictive solitaire game Freecell
    * [tetris][tetris]: A text-mode tetris game
    * [cmatrix][cmatrix]: Terminal based "The Matrix" like implementation

目前就玩到這樣。而 Raspberry Pi 除了裝 Android 比較麻煩，上面的設定也都差不多。

目前這樣就可以取代我大部分桌機的功能了 (看來我很少在用桌機)，期待未來單板電腦的效能越來越強大!

[Tinker-Board-S]: https://www.asus.com/tw/Single-Board-Computer/Tinker-Board-S/
[volumio]: https://volumio.org/get-started/
[lakka]: http://www.lakka.tv/
[libreelec]: https://libreelec.tv/downloads_new/rockchip/
[TinkerBoardOS]: https://www.asus.com/tw/Single-Board-Computer/Tinker-Board-S/HelpDesk_Download/
[dotfiles]: https://github.com/Chienweichih/dotfiles
[tig]: https://github.com/jonas/tig
[youtube-dl]: https://github.com/ytdl-org/youtube-dl/
[ccal]: http://ccal.chinesebay.com/ccal/ccal.htm
[freecell]: https://www.linusakesson.net/software/freecell.php
[tetris]: https://github.com/jserv/tetris
[cmatrix]: https://github.com/abishekvashok/cmatrix
