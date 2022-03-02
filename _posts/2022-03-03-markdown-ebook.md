---
layout: post
title: "用 Markdown 做電子書"
date: 2022-3-3 0:0:00 +0800
tags: [Markdown]
comments: true
share: true
---

前一篇文章介紹 Markdown 的三個工具，這次再來介紹製作電子書的方法

# [Pandoc][Pandoc]

前一次介紹過的 Pandoc，這次的用法是把 Markdown 轉成 EPUB

``` shell
$ pandoc input.md -o output.epub
```

可以在 Markdown 裡加上 yaml 標籤來增加一些資訊，像 title, author, lang ...

# KindleGen

透過 KindleGen 可以把 EPUB 轉成 Kindle 可以用的 mobi 檔案

不過在 Amazon 的網站上已經不能直接下載了，可以先安裝 [Kindle Previewer][KP]，然後在安裝路徑就能找到 kindlegen.exe 了

``` shell
$ kindlegen input.epub
```

# [Kindle Comic Converter][KCC]

這個工具可以把漫畫壓縮檔轉成 Kindle 的 mobi (或 Kobo 的 epub)，相關用法可以參考 [wiki page][KCC-WIKI]

整理好資料夾結構可以做出好看的目錄，添加 ComicInfo.xml 可以讓電子書有更多資訊



[Pandoc]: https://pandoc.org/
[KP]: https://www.amazon.com/Kindle-Previewer/b?node=21381691011
[KCC]: https://kcc.iosphe.re/
[KCC-WIKI]: https://github.com/ciromattia/kcc/wiki

