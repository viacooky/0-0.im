---
title: Hello World
date: 2024-02-21T09:14:22+08:00
lastmod: 2024-02-21T12:49:17+08:00
# type: posts
draft: true
type: posts
# tags:
# - Windows
categories:
  - 未分类
---

## Hello World

![Windows](https://img.shields.io/badge/Windows-black?logo=windows&logoColor=0078D4)
![License](https://img.shields.io/badge/license-免费软件-0078D6)
![Linux](https://img.shields.io/badge/Linux-black?logo=linux&logoColor=FCC624)
![shell](https://img.shields.io/badge/Shell-Bash-blue)
![License](https://img.shields.io/github/license/Bash-it/bash-it)

## 代码块 拓展语法

```bash {title="100MB"}
curl https://speed.cloudflare.com/__down?bytes=104857600 > /dev/null
```

## center-quote

[参考](https://fixit.lruihao.cn/zh-cn/documentation/content-management/shortcodes/extended/introduction/#center-quote)

{{< center-quote >}}
**hello** _world_
this is a center-quote shortcode example.
{{< /center-quote >}}

```
{{< center-quote >}}
**hello** *world*
this is a center-quote shortcode example.
{{< /center-quote >}}
```

## 横幅

[参考](https://fixit.lruihao.cn/documentation/content-management/shortcodes/extended/introduction/#admonition)

type 支持以下：

- note
- abstract
- info
- tip
- success
- question
- warning
- failure
- danger
- bug
- example
- quote

{{< admonition type=tip title="This is a tip" open=false >}}
一个 **note** 横幅
{{< /admonition >}}

```
{{< admonition type=tip title="This is a tip" open=false >}}
一个 **技巧** 横幅
{{< /admonition >}}
```

## link

[参考](https://fixit.lruihao.cn/zh-cn/documentation/content-management/shortcodes/extended/introduction/#link)

{{< link href="/music/Wavelength.mp3" content="Wavelength.mp3" title="Download Wavelength.mp3" download="Wavelength.mp3" card=true >}}

```
{{< link href="/music/Wavelength.mp3" content="Wavelength.mp3" title="Download Wavelength.mp3" download="Wavelength.mp3" card=true >}}
```

{{< link href="https://github.com/hugo-fixit/FixIt" content="FixIt Theme" title="source of FixIt Theme" card=true >}}

```
{{< link href="https://github.com/hugo-fixit/FixIt" content="FixIt Theme" title="source of FixIt Theme" card=true >}}
```
