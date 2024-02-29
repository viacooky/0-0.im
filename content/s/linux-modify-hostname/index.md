---
title: Linux - 修改主机名
date: 2024-02-26T14:16:33+08:00
lastmod: 2024-02-26T14:16:33+08:00
type: posts
tags:
  - bash
  - ssh
categories:
  - Linux
---

### 查看主机名

```bash
hostnamectl status
```

### 修改主机名

```bash
# 修改主机名
hostnamectl set-hostname XXXX
# 刷新bash
source ~/.bashrc
```
