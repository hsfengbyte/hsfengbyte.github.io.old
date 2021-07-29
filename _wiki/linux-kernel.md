---
layout: wiki
title: Linux Kernel
categories: Linux
description: 类 Unix 系统下的一些常用命令和用法。
keywords: Linux
---

## 文档

### 内核日志级别

日志级别一共有8个级别，printk的日志级别定义如下（在include/linux/kernel.h中）：

```c
#define KERN_EMERG 0
#define KERN_ALERT 1
#define KERN_CRIT 2
#define KERN_ERR 3
#define KERN_WARNING 4
#define KERN_NOTICE 5
#define KERN_INFO 6
#define KERN_DEBUG 7
```

## 工具

### NFS

安装NFS软件包

```shell
sudo apt install nfs-kernel-server
sudo apt install nfs-common
```

添加NFS共享目录

```shell
# sudo vim /etc/exports
/path *(rw,sync,no_root_squash)

# sudo chmod -R 777 /path
```

测试NFS服务器

```shell
sudo mount -t nfs 127.0.0.1:/path /mnt -o nolock
```

### 其它软件

通信软件

- mutt + msmtp

代理软件

- proxychains

## Q & A


### archlinux如何快速切换中国源？

```
pacman-mirrors --country China
```