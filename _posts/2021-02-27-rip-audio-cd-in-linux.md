---
layout: post
title: "在 Linux 上擷取音樂 CD"
date: 2021-2-27 23:35:00 +0800
tags: [tools]
comments: true
share: true
---

想要在 Linux 上擷取音樂 CD，有一個很強大的工具: [abcde - A Better CD Encoder][abcde]

這篇文章就要來介紹如何安裝、設定 abcde

# 安裝 #

除了安裝 abcde 程式，還需要安裝一些編碼器。在我使用的設定裡有：oggenc, lame, flac, mpcenc, fdkaac, opusenc, wavpack, mac, tta, twolame, ffmpeg

大部分的程式，都能用 apt-get 安裝，有：

``` shell
$ sudo apt-get install abcde
$ sudo apt-get install lame
$ sudo apt-get install flac
$ sudo apt-get install wavpack
$ sudo apt-get install twolame
$ sudo apt-get install ffmpeg
$ sudo apt-get install opus-tools      # for opusenc
$ sudo apt-get install musepack-tools  # for mpcenc
```

剩下這三個在我的 Debian 系統上找不到能夠直接安裝的，所以我就從 source build 了

1. fdkaac

    這個需要先 build library, 再 build frontend

    library 是這個 [mstorsjo/fdk-aac][mstorsjo]

    frontend 是這個 [nu774/fdkaac][nu774]  

    build 的方法是：

    ``` shell
    $ autoreconf -i
    $ ./configure --prefix=$HOME/usr && make && make install
    $ # ($HOME/usr 是我個人使用的安裝路徑)
    ```

    補充一個設定 environment variables 的小知識，在 build 需要用到 library 前：

    ``` shell
    $ export CPPFLAGS='-I/.../usr/include/'
    $ export LDFLAGS='-L/.../usr/lib/'
    ```

    這樣設定才能讓需要用到這個 library 的程式找到他的路徑

2. mac

    mac 是這個 [fernandotcl/monkeys-audio][fernandotcl]

    build 的方法是：

    ``` shell
    $ cmake .
    $ make DESTDIR=$HOME install
    ```

    最後 build 出的結果就會跑到 $HOME/usr/local/bin 的目錄

3. tta

    tta 是這個 [TTA Lossless Audio Codec][tta]

    build 的方法是：

    ``` shell
    $ ./configure --prefix=$HOME/usr && make && make install
    ```

安裝的步驟終於大功告成

# 執行 #

執行前，先準備好一份 $HOME/.abcde.conf，我把我使用的設定放在這篇文章的最後面

再來就可以擷取音樂CD了

譬如說想要擷取出 flac 的格式，就使用這個指令：

``` shell
$ abcde -o flac
```

這樣就開始執行了。最後完成的結果會放到 $HOME/Music/flac，可以開心聽音樂了!

---

同場加映 [Kid3 - Audio Tagger][kid3]

這個工具是用來修改音樂檔案的 tags，簡單好用

安裝的方式是

``` shell
$ sudo apt-get install kid3
```

---

我的 .abcde.conf：

<script src="https://gist.github.com/Chienweichih/0029fed3d63d46a2b0f0f27036f76028.js"></script>

[abcde]: https://abcde.einval.com/wiki/
[mstorsjo]: https://github.com/mstorsjo/fdk-aac
[nu774]: https://github.com/nu774/fdkaac
[fernandotcl]: https://github.com/fernandotcl/monkeys-audio
[tta]: https://sourceforge.net/projects/tta/
[kid3]: https://kid3.kde.org/
