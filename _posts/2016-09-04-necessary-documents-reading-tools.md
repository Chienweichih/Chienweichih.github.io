---
layout: post
title: "Windows, Ubuntu 系統上的文件閱讀三寶"
description: "閱讀 PDF 文件的好幫手"
date: 2016-09-04 00:15:00 +0800
tags: [tools]
comments: true
share: true
---

不是馬路三寶!! 這裡要講的是我最近找到的一些好用的工具 XD

最近都一直在讀Spec，看電腦螢幕看到眼睛受不了，於是找了許多方便的工具！主要是以下三種軟體：PDF Reader、螢幕顏色反轉 (反白)、以及翻譯軟體，接下來我就一一介紹這些工具與來源：

---

### [第一寶] PDF Reader
文件都是PDF檔，所以要先有個好用的PDF Reader。

在Ubuntu上，我用的是 [Okular][Okular] 這個軟體，可以從官網下載source來編譯，或是懶懶的用apt安裝：

``` shell
$ sudo apt-get update
$ sudo apt-get install okular
```

然後Windows上，我用PDF-XChange Viewer。而PDF-XChange Viewer從[阿榮福利味下載的免安裝版][PDF-XChange Viewer]對翻譯軟體的使用比較支援，官方網站下載安裝的就有點不行，我也不太懂為什麼。

總之就不推薦用官網下載的PDF-XChange Viewer了，要安裝不如就直接用常見的Adobe的Reader，讀者可以都安裝來比較看看。

---

### [第二寶] 螢幕顏色反轉 (反白)
白底黑字看久了眼睛超難過，如果把整個螢幕顏色反轉的話就可以讀得很舒服了！

在Ubuntu，使用Xcalib，這一次也是用apt安裝：

``` shell
$ sudo apt-get update
$ sudo apt-get install xcalib
```

然後在終端機執行：

``` shell
$ xcalib -i -a
```

螢幕顏色就黑白反轉了！ 很棒吧

可以把剛剛的指令加到鍵盤快捷鍵，這樣比較方便切換。

而在Windows上，我用 [NegativeScreen][NegativeScreen] 。

下載下來執行就可以囉！ 用 `Win + Alt + n` 的快捷鍵切換模式，對其他的快捷鍵有興趣的話就去找他的Readme來研究看看吧。

---

### [第三寶] 翻譯軟體
看英文文件，若需要查生字，離開文件查字典切來切去，實在很沒效率，而且影響閱讀的流暢度。

因此，若有查字典的工具，可以不用離開文件，把滑鼠移過去就可以查，那就太方便了！

介紹這個好用的工具: [GoldenDict][GoldenDict] ，這個軟體在Ubuntu和Windows上都可以使用，而且提供很多字典可以下載，雖然界面陽春，但是該有的功能都有了。

Ubuntu 上安裝的方式也是用apt來安裝:

``` shell
$ sudo apt-get update
$ sudo apt-get install goldendict
$ sudo apt-get install goldendict-wordnet
```

在Windows上，從他官網的下載頁下載:  
[http://goldendict.org/download.php][GD_download]  

安裝好之後，再下來字典，從這裡下載:  
[http://goldendict.org/dictionaries.php][GD_dic]  

我推薦Babylon (.bgl) dictionaries這個的字典，原因是...因為其他的都沒辦法下載了，所以只能選這個了 ╰(〒皿〒)╯ 

進去babylon-software的網頁之後，選 `languages > chinese`

然後我用的是 `Babylon English-Chinese (T)` 和 `漢字基因字典` 這兩個，按 `Add this Glossary` 就可以下載了。我這兩個一個拿來查英文，一個拿來查倉頡，其他的有興趣也可以下載下來嘗試看看。

下載了字典檔之後就把他加到程式的資料庫裡吧，在最上面的選單 `編輯 > 字典` ，然後 `字典來源 > 檔案 > 新增` ，把你的字典在的資料夾位置加進來，按重新掃描就完成了！

如果你用的是portable版，你要把你的字典資料放到 `content 資料夾` 裡，一樣重新掃描就OK了！

![dic]({{ site.baseurl }}/images/2016-09-04-necessary-documents-reading-tools/dic.png)
{: .center}

在 `編輯 > 偏好設定` 那裡可以設定一些快捷鍵或螢幕取詞什麼的東西，這裡就不詳細介紹了，很簡單的自己研究看看吧。

好像太懶了，總之，有什麼問題的話在下面留言也可以，Google上也很多資料，就這樣了（好敷衍）。

這樣就完成了！你就有超方便的字典可以查囉！

我在Ubuntu上是按著Ctrl，把要查的字劃記起來就可以查了;或是Ctrl+C複製資料的同時也會翻譯，這個有時候比較麻煩，又不是每次複製的時候都要翻譯，但是又不知道怎麼把他關掉，所以就只能關程式解決了。

而在Windows上，也是可以複製的時候即時翻譯，有些軟體上 (像免安裝的PDF-XChange Viewer) 可以按著Ctrl+滑鼠移到字上面就翻譯，這樣就方便很多。

如果用不習慣GoldenDict，在Windows上還有另一個選擇： [Lingoes][Lingoes] ，這也是個好用的翻譯軟體，不過只有Windows版，而且沒有倉頡字典，有興趣的話還是可以下載來玩看看！

以上就是我推薦的好用文件閱讀三寶！ 有問題或其他建議歡迎在下面留言討論呦！

[Okular]: https://okular.kde.org/
[PDF-XChange Viewer]: http://www.azofreeware.com/2007/10/pdf-xchange-viewer-1026.html
[NegativeScreen]: http://arcanesanctum.net/negativescreen/
[GoldenDict]: http://goldendict.org/
[GD_download]: http://goldendict.org/download.php
[GD_dic]: http://goldendict.org/dictionaries.php
[Lingoes]: http://www.lingoes.cn/
