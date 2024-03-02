---
title: ssh - 设置免密码登录
date: 2024-02-26T12:49:17+08:00
lastmod: 2024-02-26T12:50:17+08:00
type: posts
tags:
  - ssh
categories:
  - Windows
  - Linux
---

## 1.目标机器

### 1.1 root 用户登录目标机器

```bash
ssh root@hostname
```

### 1.2 修改 sshd 配置文件

配置文件路径 `/etc/ssh/sshd_config`

```text
PubkeyAuthentication yes #启用公钥私钥配对认证方式
AuthorizedKeysFile .ssh/authorized_keys #公钥文件路径
PasswordAuthentication no #可选，关闭密码登录，提高安全性
```

### 1.3 重启 SSH 服务

```bash
systemctl restart sshd
```

---

## 2. 客户端机器

### 2.1 生成密钥对（如果已经有密钥对，跳过此步）

```bash
ssh-keygen -t rsa
```

### 2.2 将公钥发送到服务端机器

#### 2.2.1 ssh-copy-id 方式

Linux 系统上可以使用以下命令

```bash
# ssh-copy-id -i PUB_PATH root@SERVER_IP
ssh-copy-id -i /root/.ssh/id_rsa.pub root@8.8.8.8
```

#### 2.2.2 手动拷贝方式

文本方式打开 `id_rsa.pub` 文件，将公钥复制到目标机器的 `.ssh/authorized_keys` 中

`id_rsa.pub` 路径:

- Windows 系统中，一般在 `C:\Users\用户名\.ssh\`目录下
- Linux 系统中，一般在 `~/.ssh/` 目录下

### 2.3 测试验证

```bash
ssh root@8.8.8.8
```

---

## 3. 使用别名登录，懒得输 IP （可选）

### 3.1 设置 ssh config

格式：

|              |                   |
| ------------ | ----------------- |
| Host         | 别名              |
| HostName     | 主机名，IP 或域名 |
| User         | 用户名            |
| Port         | 端口              |
| IdentityFile | 指定私钥路径      |

- Windows： `C:\Users\用户名\.ssh\config` 没有的话新建一个

  ```text
  Host HK01
      HostName 8.8.8.8
      User root
      Port 22
      IdentityFile C:\Users\aaa\.ssh\id_rsa
  ```

- Linux： `~/.ssh/config` 没有的话新建一个
  ```text
  Host HK01
      HostName 8.8.8.8
      User root
      Port 22
      IdentityFile ~/.ssh/id_rsa
  ```

### 3.2 使用

设置好后，可以用 Host 名称进行登录，省得填 IP

```bash
ssh root@HK01
```
