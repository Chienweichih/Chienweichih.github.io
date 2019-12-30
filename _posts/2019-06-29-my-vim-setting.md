---
layout: post
title: "我的 Vim 設定"
date: 2019-06-29 23:50:00 +0800
tags: [vim]
comments: true
share: true
---

這篇文章整理我的 Vim 設定，是個適合寫 C 語言的環境設定

先放一張圖，這是設定完的樣子:

![my_vim_setting]({{ site.baseurl }}/images/2019-06-29-my-vim-setting/vim.png){: .center-image}

如果你對 Vim 的指令沒有很熟悉，我推薦你先閱讀這本 [Practical Vim][practical_vim]  
讀完這本書就可以掌握 Vim 的操作  
這篇文章沒有介紹 Vim 的使用方法，只有我的設定整理

---

需要安裝的程式有:

1. [Vim][vim]
2. [Exuberant Ctags][ctags]
3. [GNU Global][global]

最後加上 [Plugins][dotfiles]

# Vim #

就是把 Vim 安裝起來，我現在用的是 Git Bash 裡面附的 Vim

# Ctags #

在 [Practical Vim][practical_vim] 的 Chapter 16 介紹了 Index and Navigate 的工具，ctags

使用前先在 Project 的最上層目錄執行:
> `ctags -R`

生成 tags 檔

用 `<C-]>` 可以跳到游標下 keyword 的定義，用 `<c-t>` 跳回來查詢之前的位置  
搭配 [Taglist][taglist] 這個 plugin，可以像前面的範例圖一樣把 tags 列在左邊的視窗

# Global #

這是一個 source code tagging system，我拿他來當作 Project Search 的工具，  
像 vimgrep 的功能

使用前先在 Project 的最上層目錄執行:
> `gtags`

生成 GPATH、GRTAGS 和 GTAGS 檔

用 `:Gtags -g <pattern>` 就可以在整個 Project 裡搜尋你要的 pattern，  
並且將結果放到 Quickfix List，像前面的範例圖下方的視窗一樣  
( Quickfix List 的操作可以參考 [Practical Vim][practical_vim] 的 Tip 106 )

# Plugins #

我的 Plugins 設定放在我的 [dotfiles][dotfiles] 的 .vim 目錄裡

這裡有前面提到的 taglist 和 gtags 的設定  
還有一些是 [Practical Vim][practical_vim] 裡面介紹的 Plugins，是作者 [Drew Neil][nelstrom] 和 [Tim Pope][tpope] 的設定  
配色我用的是 [PaperColor Theme][papercolor]

安裝 Plugins 的方法，在 Vim 8 之後變得很簡單：  
把 [dotfiles][dotfiles] clone 下來，接著用這個指令把其他 submodule 都下載下來：
> `git submodule update --init --recursive`

最後把 .vim 資料夾複製到家目錄，如果是用 Windows 的 GVim ，  
就把 .vim 改名為 vimfiles  
這樣就設定完成了，如果要確認 Vim 有沒有載入你設定的 Plugins，執行：
> `:scriptname`

就可以看到了

---

以上就是我的 Vim 的設定，終於在 2019 年底讀完 [Practical Vim][practical_vim]，然後更新這篇文章了！

[practical_vim]: https://pragprog.com/book/dnvim2/practical-vim-second-edition
[vim]: https://www.vim.org/download.php
[ctags]: http://ctags.sourceforge.net/
[taglist]: http://vim-taglist.sourceforge.net/
[global]: https://www.gnu.org/software/global/
[dotfiles]: https://github.com/Chienweichih/dotfiles
[nelstrom]: https://github.com/nelstrom
[tpope]: https://github.com/tpope
[papercolor]: https://github.com/NLKNguyen/papercolor-theme

