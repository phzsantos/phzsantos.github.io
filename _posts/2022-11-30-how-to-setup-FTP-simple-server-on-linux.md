---
author:
  name: Paulo Henrique Zanoteli Santos
title: How to setup FTP simple server on linux
date: 2022-11-30 10:00:00 UTC-3
categories: [Guides, Linux]
tags: [install-guide, config-guide, ftp]
---

# Don't use root user

- You can't acess ftp if you only have **root** user, you gonna need to create another user

## 1 - Install proftpd on linux server

```shell
sudo apt install proftpd
```

## 2 - Install FileZilla on client machine

Linux:

```shell
sudo apt install filezilla
```

Windows:

[FileZilla link](https://filezilla-project.org/ "FileZilla Official WebSite")

**Installation:** next, next, finish.

## 3 - Open FileZilla

Fill out: 
- Host: **your server ip**
- Username: **your user (same of the linux login)**
- Password: **your password (same of the linux login)** 
- Port: **21** 

![Upload 1](/assets/img/posts/2022-11-30-how-to-setup-FTP-simple-server-on-linux/1.png)

**Quickconnect**, you're in.

