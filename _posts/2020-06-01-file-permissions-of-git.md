---
layout: post
title: "救命 我的檔案被 Git 修改權限"
date: 2020-6-1 23:40:00 +0800
tags: [git, permission, access denied, cygwin]
comments: true
share: true
---

如標題所言，最近被 Git 玩弄得很慘  
程式碼目錄突然被修改了權限，讓我不能新增刪除檔案，編譯的時候就卡住了

於是我使用 Git 還原大法：把檔案全部刪除，再用 `git reset --hard` ，結果還是一樣  
(還要先 chmod 才能用 Windows 資料夾刪檔案)

我開始找資料，整理了各家說法之後終於找到了解答

----------

原來 Git 會記錄一套特別的檔案權限，使用這個 command 可以列出檔案的權限：

> `git ls-files --stage`

* 100644 是一般的檔案，這就是讓我不能修改及編譯的元兇
* 100755 是可執行的檔案

想要修改權限，可以用 `update-index` 的 Git command，但是我想把整個目錄下的檔案一次全部變成可執行的權限

那就這麼做：

> `git add --chmod=+x .`

最後再 commit 就完成了！  
(如果資料夾還是不能新增檔案，那就把檔案全部複製到另一個資料夾，新的資料夾就沒有問題了)

以前用 [Windows 版的 Git][Git] 沒碰過這樣的問題，後來改用 Cygwin 的 Git 就碰到了  
還好找到了解法，以後不用再害怕檔案被 Git 修改權限了

----------

Reference:  
[https://stackoverflow.com/a/40979016](https://stackoverflow.com/a/40979016)  
[https://git-scm.com/docs/git-update-index](https://git-scm.com/docs/git-update-index)

[Git]: https://git-scm.com/
