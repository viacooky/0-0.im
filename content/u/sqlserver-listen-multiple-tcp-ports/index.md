---
title: SQL Server - 将数据库引擎配置为侦听多个 TCP 端口
date: 2024-03-01T11:10:51+08:00
lastmod: 2024-03-01T11:10:51+08:00
type: posts
tags:
  - sql
  - SQL Server
categories:
  - Windows
---

{{< center-quote >}}
**本主题说明如何使用 SQL Server 配置管理器在 数据库引擎 中将 SQL Server 配置为侦听多个 TCP 端口。**
{{< /center-quote >}}

## 步骤

### 1. 打开`SQL Server 配置管理器`

打开 `SQL Server 配置管理器`，展开 `SQL Server 网络配置`，找到 <实例> 协议 `TCP/IP`，右键属性

![](./1.png)

### 2. 修改监听端口

打开 `IP 地址` - `IPALL`，在 `TCP Ports` 中，输入需要监听的端口

{{< admonition type=tip title="多个端口配置" open=true >}}
多个端口，用逗号隔开

例如：`1433,21433`
{{< /admonition >}}

![](./2.png)

### 3. 重启服务

`SQL Server 配置管理器` 中，找到 `SQL Server 服务`，找到实例，右键重启

![](./3.png)

## 参考

{{< link href="https://learn.microsoft.com/zh-cn/sql/database-engine/configure-windows/configure-the-database-engine-to-listen-on-multiple-tcp-ports?view=sql-server-ver16#to-configure-the-sql-server-database-engine-to-listen-on-an-additional-tcp-port" content="微软官方文档" title="微软官方文档" card=true >}}
