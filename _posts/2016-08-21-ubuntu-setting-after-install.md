---
layout: post
title: "Ubuntu 系統安裝後的一些設定"
description: "其實不限於 Ubuntu, 有些 Linux 都通用"
date: 2016-08-21 22:10:16 +0800
tags: [tools]
comments: true
share: true
---

昨天把筆電的 120G SSD 全部清掉拿來裝 [Ubuntu 16.04.1 LTS][Ubuntu 16.04.1 LTS] <del>（受不了Windows了）</del>。現在終於弄的差不多了，來把碰到的一些問題還有設定紀錄一下吧！  
（我在安裝的時候選擇搭配[LVM][LVM]，感覺好像是很厲害的東西，可是現在不太懂他是怎麼運作的，裝了以後跟以前比好像開機慢了一點點，以後瞭解的話再補充吧）

以下就是一項一項的問題，都有附上我查到的reference，所以我就寫的簡短一點（絕對不是因為很懶）

---

### 安裝 Google Chrome
reference: [http://askubuntu.com/a/221343][chrome]
{: .right}

Chrome是個好用的瀏覽器，我的紀錄跟安裝的應用程式只要登入Google帳號就全部同步好了，可是Ubuntu沒有內建Chrome，所以就來把他裝起來。

首先，要啟用"universe" repository，然後：

``` shell
$ sudo apt-get update
$ sudo apt-get install libgconf2-4 libnss3-1d libxss1
```

就可以去Chrome的網站下載安裝google-chrome-stable了

---

### 使用 ibus 中文輸入法
reference: [http://it.livekn.com/2016/05/ubuntu-1604-ibus.html][ibus]
{: .right}

Ubuntu的中文輸入法我還是比較習慣用ibus，在16.04預設是沒有ibus的，所以就來把ibus裝起來。

``` shell
$ sudo apt-get install ibus-zhuyin #注音輸入法
$ sudo apt-get install ibus-table-cangjie-big #倉頡輸入法
```

然後重新啟動ibus

``` shell
$ ibus restart
```

最後去設定，文字輸入的地方把ibus加進來就OK了！

---

### NumLock 開機後不會自動啟用 （右側九宮格數字鍵）
reference: [https://ubuntuforums.org/showthread.php?t=2218111&p=12998553#post12998553][numlock]
{: .right}

鍵盤旁邊的九宮格數字鍵在開機後是關掉的，這很麻煩，一定要設定一下！

首先，安裝 numlockx

``` shell
$ sudo apt-get update
$ sudo apt-get install numlockx
```

然後修改 `/usr/share/lightdm/lightdm.conf.d/50-unity-greeter.conf`，最後一行加上

``` shell
$ greeter-setup-script=/usr/bin/numlockx on
```

重開機就OK了！

---

### 安裝 LaTeX
reference: [http://milq.github.io/install-latex-ubuntu-debian/][latex]
{: .right}

LaTeX是個很棒的東西，我都拿它來做投影片，所以電腦裡也安裝一下編輯的工具吧！

首先先安裝texlive-full，這個會安裝超久的（下載的東西有3GB那麼多吧）

``` shell
$ sudo apt-get install texlive-full
```

安裝完後，裝texmaker編輯器

``` shell
$ sudo apt-get install texmaker
```

這樣就可以開始做投影片囉！

---

### 將中文資料夾改成英文
reference: [https://www.ubuntu-tw.org/modules/newbb/viewtopic.php?post_id=306796#forumpost306796][user-dir]
{: .right}

中文的資料夾名在terminal使用時很不方便，所以想把他全部改成英文

首先先確認目前使用的語系

``` shell
$ echo $LANG
```

然後將語系變更為英文

``` shell
$ export LANG=en_US
```

執行這個更改資料夾名稱

``` shell
$ xdg-user-dirs-gtk-update
```

再把語系改回原本使用的語系

``` shell
$ export LANG=最前面記的
$ # 我的是 zh_TW.UTF-8
```

最後再執行一次更名，但是這次選擇保留舊名稱

``` shell
$ xdg-user-dirs-gtk-update
```

這樣就OK了！

---

### Jekyll 安裝
reference: [https://www.howtoinstall.co/en/ubuntu/xenial/jekyll][jekyll]
{: .right}

上一篇文章有貼一篇安裝 Jekyll的方法，不過這次查到更簡單、更方便的方法，紀錄一下

``` shell
$ sudo apt-get update
$ sudo apt-get install jekyll
```

就這樣！天阿，超方便！我之前安裝那麼久到底在幹麻

不過這好像是16.04才開始有的方法

2017-07-27 update: Raspberry pi (Raspbian) 也可以這樣裝耶，超方便

---

### Git 初始設定
reference: [https://git-scm.com/book/en/v2/Getting-Started-First-Time-Git-Setup][git-setup]
{: .right}

使用Git前先設定一下初始的設定

``` shell
$ git config --global user.name "yourname"
$ git config --global user.email youremail@example.com
$ git config --global core.editor vim
```

我主要就設定這三項

---

### Github 新增 SSH key
reference: [https://help.github.com/articles/generating-an-ssh-key/][github-ssh]
{: .right}

用SSH push pull github的東西比較方便，設定一下如何加SSH key

先查一下有沒有存在的SSH key

``` shell
$ ls -al ~/.ssh
```

剛安裝好應該是沒有吧，來建立一個新的key吧

``` shell
$ ssh-keygen -t rsa -b 4096 -C "your_email@example.com"
```

然後他問你key要存哪裡，直接按Enter。然後輸入你要的密碼

再來確認ssh-agent有沒有啟動

``` shell
$ eval "$(ssh-agent -s)"
```

加入剛剛新增的key

``` shell
$ ssh-add ~/.ssh/id_rsa
```

最後是將這個key加到Github的設定，先把key複製起來

``` shell
$ sudo apt-get install xclip
$ xclip -sel clip < ~/.ssh/id_rsa.pub
```

最後去Github的設定找New SSH key的地方，將key加入就OK了！

這裡寫的步驟比較簡短，若要詳細的介紹的話請看一下reference的網站吧！

---

用到現在，目前就碰到這些設定跟問題了，紀錄一下，以後就不用再查一次了。

PS: 上班三個禮拜了，看了兩本好厚的書，之後應該會整理一些 NAND Flash 技術的文章吧，如果我沒有很懶的話XD 哈哈

[Ubuntu 16.04.1 LTS]: http://releases.ubuntu.com/16.04.1/
[LVM]: https://en.wikipedia.org/wiki/Logical_Volume_Manager_(Linux)
[chrome]: http://askubuntu.com/a/221343
[ibus]: http://it.livekn.com/2016/05/ubuntu-1604-ibus.html
[numlock]: https://ubuntuforums.org/showthread.php?t=2218111&p=12998553#post12998553
[latex]: http://milq.github.io/install-latex-ubuntu-debian/
[user-dir]: https://www.ubuntu-tw.org/modules/newbb/viewtopic.php?post_id=306796#forumpost306796
[jekyll]: https://www.howtoinstall.co/en/ubuntu/xenial/jekyll
[git-setup]: https://git-scm.com/book/en/v2/Getting-Started-First-Time-Git-Setup
[github-ssh]: https://help.github.com/articles/generating-an-ssh-key/
