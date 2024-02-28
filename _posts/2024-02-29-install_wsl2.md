---
layout: post
title: "安裝 WSL2 超簡單"
date: 2024-2-29 00:00:00 +0800
tags: [Windows, Ubuntu]
comments: true
share: true
---

都 2024 年了還有人沒玩過 WSL 嗎？ 有，就是我


WSL 的全名是 Windows Subsystem for Linux，現在已經到第二版了。當初 WSL 剛登場的時候，其安裝步驟之繁瑣讓我望而卻步，如今發現 WSL 的安裝已經變得相當簡單了，今天輕輕鬆鬆的就把他給裝好了

超簡單，只要一個指令就安裝完成了：

> `wsl --install`

然後再安裝這個比較好看的 [Windows Terminal][windows-terminal]

重開機之後，就有一個完整功能的 Ubuntu 可以用了！

其他軟體的安裝，可以參考這篇：

> [2023 年 Linux 安裝軟體 (Flatpak)][2023-08-16]

---


有關 WSL 的詳細說明，這裡整理的很詳細，有興趣的人可以看看這個 [Awesome-WSL][awesome-wsl]

目前用起來很棒，安裝軟題就用 apt，基本上跟 Ubuntu 沒兩樣，我沒有用到需要 GUI 的軟體

記憶體的使用還蠻多的，至少都會用超過 1G 以上

然後執行某些 bat 檔會怪怪的，可能會直接卡死，要重開 wsl 才能解決，問題還是有的

最後有個 [issue][wsl2-issue]：如果要在 WSL2 讀取 WSL 系統之外的檔案，因為 ext4 virtual disk 在 NTFS 上的原因，檔案讀取會變得比較慢。如果要解決這個問題，可以把 WSL 的版本降為 WSL1，都是 NTFS 就不會有讀取太慢的問題了

整體來說，還是比 Git Bash 好用很多，就繼續玩看看吧



[windows-terminal]: https://github.com/microsoft/terminal
[2023-08-16]: {{ site.baseurl }}/2023_linux_flatpak
[awesome-wsl]: https://github.com/sirredbeard/Awesome-WSL
[wsl2-issue]: https://stackoverflow.com/a/68974497
