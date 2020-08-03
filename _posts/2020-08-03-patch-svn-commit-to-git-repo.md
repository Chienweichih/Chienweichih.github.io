---
layout: post
title: "從 svn 搬 commit 到 git repo"
date: 2020-08-03 17:30:00 +0800
tags: [git, svn]
comments: true
share: true
---

以下介紹在各種情況下，如何複製一個想要的 commit 到目前的 branch

### 一、同一個 repo, 不同的 branch ###

直接使用 [cherry-pick][cherry-pick]  

---

### 二、不同的兩個 git repo 之間 ###

ref: [https://yodalee.blogspot.com/2017/03/git-patch.html](https://yodalee.blogspot.com/2017/03/git-patch.html)

1. 把想搬的 commit 生成 patch

    > `git format-patch -1 <commit> # one commit`  
    > `git format-patch -n <commit> # <n> commit`  
    > `git format-patch <commit>    # commit to head`

2. 把所有 .patch 檔搬到想要 apply 的 repo，然後執行：

    > `git am *.patch`

3. 如果碰到衝突就會停下來，想要處理的話就要：

    > `git apply --reject xxx.patch`

4. 把 .rej 檔的地方修改好後：

    > `git add -u # only adds currently tracked files`  
    > `git am --continue`

最後就完成了

---

### 三、從 svn 搬 commit 到 git repo ###

如果你的工作環境用的是 svn，但是又想把 commit 搬到 local 的 git

也可以使用 patch 的方式來操作

1. 從 svn 生成 patch

    > `svn diff http://your-svn-site/... -r <revision - 1>:<revision>`

2. 可以把前面的結果導出到檔案，然後在 git repo 執行 patch command

    > `patch --binary --no-backup-if-mismatch -p0`

可以參考下面這個範例

<script src="https://gist.github.com/Chienweichih/3a3982b318dc2fe3ea766edde18fb793.js"></script>

---

### !!! ###

但是，麻煩的事情出現了

如果你是用 Windows 系統的 svn，Cygwin 的 git

autocrlf 的問題又會跑出來亂了 (different line endings)

目前我還不知道怎麼處理，期待有一天突然領悟，那我就可以再整理一篇

[https://stackoverflow.com/a/4425433/1709408](https://stackoverflow.com/a/4425433/1709408)



[cherry-pick]: https://git-scm.com/docs/git-cherry-pick
