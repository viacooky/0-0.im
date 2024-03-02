---
title: ping.pe - 知名在线网络检测服务
date: 2024-03-02T15:14:22+08:00
lastmod: 2024-03-02T15:14:22+08:00
type: posts
tags:
  - 测速
  - 检测
  - 网络
categories:
  - 服务
---

![logo](./logo.jpeg)

|          |                         |
| -------- | ----------------------- |
| 网站     | <hhttps://ping.pe>      |
| 相关信息 | <https://ping.pe/about> |
| 社区     | <https://flap.ping.pe/> |

## 简介

**ping.pe**，知名的在线网络测试服务，据说跟著名的主机商 Bandwagon Host(搬瓦工)同属 IT7 Networks Inc.旗下。

目前为止提供全球 38 个测试点。其中中国大陆地区有 13 个测试节点，包含了阿里云，腾讯云，中国移动，中国联通，中国电信，中国电信 CN2 多家 ISP 服务商。

目前主要提供 ping 测试，dig 测试和 TCP 端口测试。

## 功能

### ping

|      |                                |
| ---- | ------------------------------ |
| 格式 | `https://ping.pe/{IP 或 域名}` |
| 示例 | <https://ping.pe/8.8.8.8>      |
|      | <https://ping.pe/0-0.im>       |

### ping -ipv6

|      |                                      |
| ---- | ------------------------------------ |
| 格式 | `https://ping6.ping.pe/{IP 或 域名}` |
| 示例 | <https://ping6.ping.pe/8.8.8.8>      |
|      | <https://ping6.ping.pe/0-0.im>       |

### tcp

|      |                                           |
| ---- | ----------------------------------------- |
| 格式 | `https://tcp.ping.pe/{IP 或 域名}:{端口}` |
| 示例 | <https://tcp.ping.pe/baidu.com:443>       |
|      | <https://tcp.ping.pe/0-0.im:443>          |

### tcp - ipv6

|      |                                            |
| ---- | ------------------------------------------ |
| 格式 | `https://tcp6.ping.pe/{IP 或 域名}:{端口}` |
| 示例 | <https://tcp6.ping.pe/google.com:443>      |
|      | <https://tcp6.ping.pe/0-0.im:443>          |

### MTR（My Traceroute）

结合了 traceroute 和 ping 来测量网络路径的健康状况

|      |                                    |
| ---- | ---------------------------------- |
| 格式 | `https://mtr.ping.pe/{IP 或 域名}` |
| 示例 | <https://mtr.ping.pe/baidu.com>    |
|      | <https://mtr.ping.pe/0-0.im>       |

### MTR（My Traceroute） - ipv6

结合了 traceroute 和 ping 来测量网络路径的健康状况

|      |                                     |
| ---- | ----------------------------------- |
| 格式 | `https://mtr6.ping.pe/{IP 或 域名}` |
| 示例 | <https://mtr6.ping.pe/google.com>   |
|      | <https://mtr6.ping.pe/0-0.im>       |

### dig

DNS 记录查询

|      |                                                             |
| ---- | ----------------------------------------------------------- |
| 格式 | `https://mtr.ping.pe/{主机}:{类型}:{DNS}`                   |
|      | 主机: IP 或 域名                                            |
|      | 类型: `A`, `AAAA`, `CNAME`, `TXT`, `MX`, `NS`, `PTR`, `CAA` |
|      | DNS: 指定使用 DNS 服务器，默认 `8.8.8.8`                    |
| 示例 | https://dig.ping.pe/gp.0-0.im:CNAME                         |
|      | https://dig.ping.pe/gp.0-0.im:CNAME:223.5.5.5               |

### char

以图表形式表示 ping

|      |                                      |
| ---- | ------------------------------------ |
| 格式 | `https://chart.ping.pe/{IP 或 域名}` |
| 示例 | <https://chart.ping.pe/google.com>   |
|      | <https://chart.ping.pe/0-0.im>       |

### char - ipv6

以图表形式表示 ping

|      |                                       |
| ---- | ------------------------------------- |
| 格式 | `https://chart6.ping.pe/{IP 或 域名}` |
| 示例 | <https://chart6.ping.pe/google.com>   |
|      | <https://chart6.ping.pe/0-0.im>       |
