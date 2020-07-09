---
layout: post
title: "我的 Vim 設定 (2)"
date: 2020-07-09 17:50:00 +0800
tags: [vim]
comments: true
share: true
---

最近讀了 [Modern Vim][modern_vim]，又學了一些方便的設定，所以來把我的 Vim 設定更新一下

之前的文章在這裡 ( [我的 Vim 設定][my_vim_setting] )。舊的方法還是可以用，不過新的更好

---

# 第一步 安裝 #

我裝了這些：

1. [Vim][vim]
2. [Exuberant Ctags][ctags]
3. [ripgrep (rg)][ripgrep]

## vim ##

要安裝 8.0 以上的版本，我現在用的是 Cygwin 的 Vim

## ctags ##

在 [Practical Vim][practical_vim] Chapter 16 介紹的 Index and Navigate 工具，  
我現在用的是 Cygwin 的 ctags

使用方法：

在 Project 的最上層目錄執行

> `ctags -R`

就會產生索引用的 tags 檔。  
用 `<C-]>` 跳到游標下 keyword 的定義， `<C-t>` 跳回查詢之前的位置

## rg ##

快速搜尋文件內容的工具，可以跟後面介紹的 plugin "vim-grepper" 配合使用

---

# 第二步 Plugins #

目前使用這些：

1. [k-takata/minpac][minpac]
2. [junegunn/fzf][fzf]
3. [yegappan/taglist][taglist]
4. [mhinz/vim-grepper][vim-grepper]
5. [samoshkin/vim-mergetool][vim-mergetool]
6. [NLKNguyen/papercolor-theme][papercolor-theme]
7. [itchyny/lightline.vim][lightline.vim]
8. [justinmk/vim-syntax-extra][vim-syntax-extra]
9. [hdima/python-syntax][python-syntax]
10. [nelstrom/vim-visual-star-search][vim-visual-star-search]
11. [tpope/vim-abolish][vim-abolish]
12. [tpope/vim-fugitive][vim-fugitive]
13. [tpope/vim-surround][vim-surround]
14. [tpope/vim-unimpaired][vim-unimpaired]

## minpac ##

這是一個 vim plugin 的 package manager。  
設定好 [vimrc][vimrc]，後續的安裝和更新只要在 Vim 裡輸入一個指令：

> `:PackUpdate`

安裝 minpac 的方法：

> `mkdir -p ~/.vim/pack/minpac/opt`  
> `cd ~/.vim/pack/minpac/opt`  
> `git clone https://github.com/k-takata/minpac.git`

## fzf ##

用來搜尋檔名，不用打完整檔名的 fuzzy 搜尋。安裝方法：

> `~/.vim/pack/minpac/start/fzf/install --bin`

但是，我現在用在 Cygwin 有個 bug。解決方法很簡單，在 fzf.vim 第 587 行後面加上：

> `&& ($TERM !=# 'xterm')`

## taglist ##

可以用來看程式碼的架構，方便找 function

## vim-grepper ##

這是搜尋用的工具：非同步執行，所以他不會讓你的編輯器卡住。  
還會幫你把搜尋結果放到 Quickfix list  
搭配前面安裝的 rg，只要執行：

> `:Grepper`

就能超快速的搜尋整個專案

## vim-mergetool ##

用 Vim 處理 conflict 的工具

## NLKNguyen/papercolor-theme ##

這是一個 Vim 的 color schemes，我覺得滿好看的

## itchyny/lightline.vim ##

這是一個 Vim statusline/tabline 的 color schemes  
他裡面有 PaperColor 的樣式可以選擇

## vim-syntax-extra ##

C 語言的 syntax hightlighting extra

## python-syntax ##

Python 的 syntax hightlighting extra

## vim-visual-star-search ##

[Practical Vim][practical_vim] 的作者 [Drew Neil][nelstrom] 寫的一些方便的設定。  
譬如在 visual mode 也可以用 * 和 # 來搜尋

## Tim Pope ##

Tim Pope 大師寫的 plugins，太多了，每個都很實用。  
還在慢慢探索中，有興趣的人可以到 [Github][tpope] 上看他的作品

---

以上就是整理我最近學到的一些 Vim 的設定  
Drew Neil 寫的兩本 Vim 的書整理的非常好，淺顯易懂，全部看完之後功力大增  
非常推薦大家閱讀 Drew Neil 的 [Practical Vim][practical_vim] 和 [Modern Vim][modern_vim]

[modern_vim]: https://pragprog.com/titles/modvim/
[my_vim_setting]: https://chienweichih.github.io/my-vim-setting/
[vim]: https://www.vim.org/download.php
[ctags]: http://ctags.sourceforge.net/
[ripgrep]: https://github.com/BurntSushi/ripgrep
[practical_vim]: https://pragprog.com/titles/dnvim2/
[minpac]: https://github.com/k-takata/minpac
[fzf]: https://github.com/junegunn/fzf
[taglist]: https://github.com/yegappan/taglist
[vim-grepper]: https://github.com/mhinz/vim-grepper
[vim-mergetool]: https://github.com/samoshkin/vim-mergetool
[papercolor-theme]: https://github.com/NLKNguyen/papercolor-theme
[lightline.vim]: https://github.com/itchyny/lightline.vim
[vim-syntax-extra]: https://github.com/justinmk/vim-syntax-extra
[python-syntax]: https://github.com/hdima/python-syntax
[vim-visual-star-search]: https://github.com/nelstrom/vim-visual-star-search
[vim-abolish]: https://github.com/tpope/vim-abolish
[vim-fugitive]: https://github.com/tpope/vim-fugitive
[vim-surround]: https://github.com/tpope/vim-surround
[vim-unimpaired]: https://github.com/tpope/vim-unimpaired
[vimrc]: https://github.com/Chienweichih/dotfiles/blob/master/vimrc
[nelstrom]: https://github.com/nelstrom
[tpope]: https://github.com/tpope
