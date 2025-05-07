---
layout: post
title: "MacBook 初體驗"
date: 2024-2-21 00:25:00 +0800
tags: [system]
comments: true
share: true
---

最近得到一台好舊的 MacBook, 來記錄一下做了哪些設定


這台好舊的 MacBook Pro 是 13-inch, 2012 年中的型號，macOS 是 10.15.7 Catalina

因為版本太舊了，竟然連 [Homebrew][homebrew] 都安裝不了，所以很多程式都是用 source code build 的

---

首先第一步把系統還原，透過[官網的說明][reset-mac]一步一步完成，沒遇到什麼大問題

安裝完 Catalina 的系統之後，終端機預設的 SHELL 就是 zsh 了，所以再來安裝一下[Oh My Zsh][oh-my-zsh]

Oh My Zsh 安裝完之後，很多設定就都有了，像是 git, color theme, ...

所以我原本的 [dotfiles][dotfiles] 只要用 gitconfig, vimrc, diff-so-fancy 和 vim 的 minpac，其他跟 bash 有關的都不用設定

---

再來是安裝程式，我用終端機安裝的程式有：

* [ffmpeg](https://www.ffmpeg.org)
* [fzf](https://github.com/junegunn/fzf)
* [exuberant-ctags](http://ctags.sourceforge.net)
* [ripgrep](https://github.com/BurntSushi/ripgrep)
* [tig](https://github.com/jonas/tig)
* [freecell](https://www.linusakesson.net/software/freecell.php)
* [imagemagick](https://github.com/imagemagick/imagemagick)

都是用 source code build 的，非常辛苦，還好都很順利

然後這些是用 pip 安裝的：

* [kobodl](https://pypi.org/project/kobodl)
* [yt-dlp](https://github.com/yt-dlp/yt-dlp)
* [tldr](https://github.com/tldr-pages/tldr)

最後這些是從官網下載 dmg 檔安裝的：

* [SuperTuxKart](https://supertuxkart.net/Download)
* [LibreOffice](https://www.libreoffice.org/)
* [VLC](http://www.videolan.org)

這樣就完成了！

---

最後說一下感想吧，我這台 MacBook 雖然是很舊的機器了，但還是非常好用

終端機和系統整合的很好，command C + command V 可以在各個視窗複製貼上，open 就可以打開 Finder

輸入法也都可以在各個視窗正常使用，雖然好像是廢話，但這個是我使用 ChromeBook 會遇到的問題

但可能是因為機器太老舊的關係，書籍 APP 用起來不是很順暢，不能用 Homebrew 安裝程式也很可惜

總之呢，體驗到 Mac 的厲害了，以後要換電腦的時候應該會選 Mac 吧！



[Homebrew]: https://brew.sh
[reset-mac]: https://support.apple.com/zh-tw/HT201065
[oh-my-zsh]: https://ohmyz.sh
[dotfiles]: https://github.com/Chienweichih/dotfiles
