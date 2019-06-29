---
layout: post
title: "我的VIM設定"
date: 2019-06-29 23:50:00 +0800
tags: [vim, Windows]
comments: true
share: true
---

這一篇文章，是整理我目前的 Vim 設定  
全部在 Windows 環境中使用，主要參考了這個網站的教學：  
[http://ivan7645.github.io/2016/07/12/vim_to_si/](http://ivan7645.github.io/2016/07/12/vim_to_si/)

設定完就可以有很多類似 Source Insight 的功能，大概長這個樣子：  

![my_vim_setting]({{ site.baseurl }}/images/2019-06-29-my-vim-setting/vim.png){: .center-image}

---

1. vim  
    要使用 vim，第一件事就是先安裝 vim。Windows 環境推薦使用 _gVim_ :
    > [https://www.vim.org/download.php#pc](https://www.vim.org/download.php#pc)

    下載下來，下一步到底，結束。

2. ctags  
    他能幫你建立程式碼的連結索引，讓你在函數、變數的宣告和定義之間切換

    __安裝__

    至官網下載:
    > [http://ctags.sourceforge.net/](http://ctags.sourceforge.net/)

    然後安裝，將安裝路徑加到 PATH

    __設定__

    在專案的根目錄，執行:
    > ctags -R

    就會生成索引檔案 _tags_

    要讓 vim 找到索引檔案，就要在 .vimrc 加上這個設定:
    > set tags=./tags,./TAGS,tags;~,TAGS;~

3. cscope  
    他能幫你搜尋程式碼中你想搜尋的東西，功能強大，可是我還不熟怎麼使用他

    __安裝__

    這裡有 build 好 for Windows 的 binary:
    > [https://code.google.com/archive/p/cscope-win32/downloads](https://code.google.com/archive/p/cscope-win32/downloads)

    可以將 bin 檔放到 ctag 的資料夾，剛剛設定的 path 就能找到他了

    __設定__

    在專案的根目錄，執行:
    > cscope -Rbqk

    然後在 .vimrc 設定一些會用到的設定  
    因為我還不熟，所以就先不解釋要設定什麼了

4. taglist  
    他能幫你列出檔案中的 function, struct, enum, macro...

    __安裝__

    至官網下載:
    > [http://vim-taglist.sourceforge.net/](http://vim-taglist.sourceforge.net/)

    __設定__

    也是一樣在 .vimrc 設定需要的功能，這個我就放在後面一起列出來

5. SrcExpl  
    他能讓你看游標下的那個函式或變數的宣告

    __安裝__

    至官網下載:
    > [https://github.com/wesleyche/SrcExpl](https://github.com/wesleyche/SrcExpl)

    __設定__

    繼續看下去，後面有 .vimrc 的設定

6. Trinity + NERDTree  
    可以顯示資料夾樹狀結構，而 Trinity 是讓前面三個視窗一起打開的快捷鍵

    __安裝__

    至官網下載:
    > [https://github.com/wesleyche/Trinity](https://github.com/wesleyche/Trinity)

    __設定__

    就是下面這個 .vimrc 的設定了:

7. .vimrc  
    其實他不一定要叫 .vimrc  
    只要是 vimfiles 資料夾裡面的 *.vim 檔，在 vim 開啟時都會去讀他們

    這個是我的設定
    > [https://github.com/Chienweichih/Configuration/tree/master/.vim](https://github.com/Chienweichih/Configuration/tree/master/.vim)

    所以，前面講的 taglist, SrcExpl, Trinity + NERDTree 的設定  
    我就一個一個放到這個資料夾裡面：  
    `%userprofile%\vimfiles\plugin\`

    以下整理我放了哪些 *.vim：

    * taglist.vim
    * srcexpl.vim
    * trinity.vim
    * NERD_tree.vim
        >  分別都是從前面介紹的連結下載來的

    * cscope_maps.vim  
        cscope 的設定
        > [http://cscope.sourceforge.net/cscope_maps.vim](http://cscope.sourceforge.net/cscope_maps.vim)

    * basic.vim
    * filetypes.vim  
        一些常用的基本的設定
        > [https://github.com/amix/vimrc/tree/master/vimrcs](https://github.com/amix/vimrc/tree/master/vimrcs)

    * matchit.vim  
        讓找對應的括號更聰明的設定
        > [https://github.com/benjifisher/matchit.zip](https://github.com/benjifisher/matchit.zip)

    再介紹另一個資料夾  
    這個資料夾是在前面的設定載入後，最後才會去讀的  
    `%userprofile%\vimfiles\after\`

    我放了這些設定：

    * syntax\c.vim
    * syntax\lex.vim
    * syntax\yacc.vim
    * ..\plugin\vim-syntax-extra.vim  
        程式碼 Highlight 的功能
        > [https://github.com/justinmk/vim-syntax-extra](https://github.com/justinmk/vim-syntax-extra)

    * plugin\chienweichih.vim  
        最後這是我個人的設定  
        我把 Trinity 的快捷鍵放在這裡，還有 papercolor 這個主題的設定
        > [https://github.com/NLKNguyen/papercolor-theme](https://github.com/NLKNguyen/papercolor-theme)

完成，這就是我的 Vim 的設定

---

最後分享一個我之前從別的地方看到的中文化的vimdoc，但是是簡體的，我把他轉成繁體中文:
> [https://chienweichih.github.io/vimcdoc/doc/help.html](https://chienweichih.github.io/vimcdoc/doc/help.html)

原始碼，可以放到 %userprofile%\vimfiles 裡:
> [https://github.com/Chienweichih/vimcdoc](https://github.com/Chienweichih/vimcdoc)

