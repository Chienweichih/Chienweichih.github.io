---
layout: post
title: "用 Markdown 寫文件"
date: 2021-9-12 00:25:00 +0800
tags: [Markdown]
comments: true
share: true
---

就像這個網站上所有的文章一樣，Markdown 是個方便整理文件的格式。  
最近看到了一些好用的工具，來整理一下吧!

---

# [Pandoc][Pandoc]

這是一個好用的文件轉換工具，可以把 Markdown 及其他的標記語言文檔轉換成 html, docx, TeX 等等格式，方便生成文件。

舉個例子，我目前常用的一個指令是 「把 Markdown 轉成 html」:

``` shell
$ pandoc -s input.md -o output.html
```

這樣就完成了! 其他用法請參考網站

# [Mermaid][mermaidJS]

這個是用來畫各種圖的工具，像 flowchart, sequence diagram ...。利用簡單的語法，可以生成 svg 圖檔，加到 markdown 文件裡。

他有一個[線上的編輯器][mermaid-live-editor]，什麼都不用安裝就能生成你想要的圖檔，真是非常方便又簡單。

Mermaid 的語法也請參考網站介紹

# [reveal.js][revealJS]

最後再介紹一個做簡報的工具

除了用 html，他也可以用 Markdown 的語法生成一個簡報網站

我自己的用法是使用 Python 來開一個 http server:

``` shell
# Python 3:
$ python3 -m http.server

# Python 2:
$ python -m SimpleHTTPServer
```

這樣就能在 http://127.0.0.1:8000/ 看到生成的簡報了。

---

以上這些 html 的成果，可以透過瀏覽器的列印功能做成 PDF，得到一個簡潔又漂亮的文件!



[Pandoc]: https://pandoc.org/
[mermaidJS]: https://mermaid-js.github.io/
[mermaid-live-editor]: https://mermaidjs.github.io/mermaid-live-editor/
[revealJS]: https://revealjs.com/

