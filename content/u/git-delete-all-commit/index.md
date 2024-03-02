---
title: git - 删除所有提交记录
date: 2024-02-26T16:24:23+08:00
lastmod: 2024-02-26T16:24:23+08:00
type: posts
tags:
  - git
categories:
  - Windows
  - Linux
---

有些时候强迫症发作，需要删除 git 的所有历史记录，把仓库初始化掉。

```bash
# 签出一个孤立分支 bk
git checkout --orphan bk

# 暂存更改
git add -A

# 提交更改
git commit -am "init"

# 删除 原来的 主分支 main
git branch -D main

# 将当前分支改名为 main
git branch -m main

# 强制推送
git push -f origin main
```
