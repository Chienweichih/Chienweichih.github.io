---
layout: post
title: "EPUB 電子書相關工具"
date: 2023-8-8 12:00:00 +0800
tags: [EPUB]
comments: true
share: true
---

EPUB 是一種電子書的檔案格式，有一個約定好的結構、以 XML 整理檔案之間的關係，然後用 zip 壓縮包裝起來。這篇文章整理了近期常用的工具， 可以製作和修改 EPUB 電子書檔案。

EPUB 電子書格式的相關知識，這裡有三篇文章寫的非常詳細：

> [從零開始的電子書-epub-零][epub0]

> [從零開始的電子書-epub-壹][epub1]

> [從零開始的電子書-epub-貳][epub2]

也可以從 W3C 的網站上取得 EPUB 的 Spec: [EPUB 3.3][epub33]

W3C 也提供了 EPUB 的[驗證工具][epub_check]，如果 EPUB 檔案上傳到 Google 圖書發生錯誤的時候，就可以用這些工具來找問題。

---

很久之前有寫過一篇 [用 Markdown 做電子書][markdown-ebook]，介紹了 Pandoc、KindleGen 和 Kindle Comic Converter。今天再來補充一些其他的資訊。

# [Kindle Comic Converter][KCC]

他們最近 Merge 了一些重要的修改，現在的工具可以選擇不處理原檔直接輸出、或是不切割圖檔。如果原檔很清楚的話就可以用這些選項。

做出來的 EPUB 檔案，在橫向螢幕時沒辦法一次顯示左右兩頁。後來在前面介紹 EPUB 的文章裡找到了答案，原來是要設定 rendition 屬性。

# KindleGen

補充一個上次沒提到的參數：

`-dont_append_source`

加上這個參數後，輸出的檔案大小就會小很多。

# [Kepubify][Kepubify]

這是一個把 EPUB 轉換成 Kobo 的 KEPUB 格式。

如果要把檔案放到 Kobo 閱讀器裡的話，先轉換成 KEPUB 會比較好。

# [Sigil][Sigil]

這是一個 EPUB editor，使用這個工具可以非常方便的修改 EPUB 內的文件。

---

再來是圖片的處理:

# [Imagemagick][Imagemagick]

這個是功能超級強大的圖片處理工具，他可以裁切、旋轉、連接、轉檔等等功能，而且執行速度非常快。可以參考官網的範例。

講到這個就想到一個類似的工具：[FFmpeg][FFmpeg]，不過他是用來處理影音檔案的。

# [Pngquant][Pngquant]

這個是壓縮 png 圖檔的工具，他可以壓縮將近 70% 左右的大小。

# [jpegoptim][jpegoptim]

這個是壓縮 jpg 圖檔的工具。

# [Inkscape][Inkscape]

這個是 svg 圖檔的編輯和轉檔工具。

# [Img2pdf][Img2pdf]

這個可以把一堆圖檔做成 PDF 檔案。

# [PDFtk][PDFtk]

這個工具可以合併和切割 PDF 檔案。



[epub0]: https://medium.com/parenting-tw/從零開始的電子書-epub-零-7b9f8676cab8
[epub1]: https://medium.com/parenting-tw/從零開始的電子書-epub-壹-72da1aca6571
[epub2]: https://medium.com/parenting-tw/從零開始的電子書-epub-貳-bb4393ad0c8
[epub33]: https://www.w3.org/TR/epub-33/
[epub_check]: https://github.com/w3c/epubcheck
[markdown-ebook]: {{ site.baseurl }}/markdown-ebook
[KCC]: https://github.com/ciromattia/kcc/releases
[Kepubify]: https://pgaskin.net/kepubify
[Sigil]: https://sigil-ebook.com
[Imagemagick]: https://www.imagemagick.org
[FFmpeg]: https://ffmpeg.org
[Pngquant]: https://pngquant.org
[jpegoptim]: https://github.com/tjko/jpegoptim/releases
[Inkscape]: https://inkscape.org/release
[Img2pdf]: https://pypi.org/project/img2pdf
[PDFtk]: https://www.pdflabs.com/tools/pdftk-the-pdf-toolkit
