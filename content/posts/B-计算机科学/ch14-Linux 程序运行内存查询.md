+++
title = 'B.Ch14-Linux 程序运行内存查询'
date = 2024-05-26T23:35:19+08:00
draft = false
categories = ["计算机科学"]
+++

科学计算程序编程时可能需要查询程序运行时的内存使用情况。

```sh
ps -aux|grep benCh3d-grid2  # 查看 benCh3d-grid2 进程的 PID, 第二列即为 PID
cat /proc/3300706/status    # 查看 PID 为 3300706 的进程的内存使用
```

科学计算代码大场景模拟时网格节点多，关注 `VMPeak` 内存占用峰值。

## 14.1 搭建 WSL-Debian 环境

```sh
wsl --install -d Debian
wsl --set-default-version 2
wget https://apt.repos.intel.com/intel-gpg-keys/GPG-PUB-KEY-INTEL-SW-PRODUCTS.PUB
# 详见 oneAPI APT 安装
sudo apt-get install intel-oneapi-compiler-fortran-2024.1
source /opt/intel/oneapi/setvars.sh
export FC=ifx
```

- [oenAPI APT安装](https://www.intel.cn/content/www/cn/zh/developer/tools/oneapi/base-toolkit-download.html?operatingsystem=linux&linux-install-type=apt)

## 14.2 记录一次 SSH 攻击

在 2024 年 10 月 14 日的早上，我通过 SSH 连接远程服务器，立马发现 CPU 使用率非常高。
我慌了，我怀疑它运行了很长时间了，于是我开始学习如何解决它。最后可行的方案是查询定时任务：

```sh
sudo readlink -f /proc/144329/exe  # 查询 PID 的程序
sudo crontab -l  # 查询 crontab
@monthly /root/.cfg/./dealer  > /dev/null 2>&1 & disown
```

并且查询恶意软件创建时间，发现它其实是我登录 SSH 的时候被攻击的：

```sh
sudo stat /root/.cfg/./dealer
  文件：/root/.cfg/./dealer
  大小：894371    	块：1752       IO 块大小：4096   普通文件
设备：fd00h/64768d	Inode：16518450    硬链接：1
权限：(0755/-rwxr-xr-x)  Uid: (    0/    root)   Gid: (    0/    root)
访问时间：2024-10-14 09:08:03.860685918 +0800
修改时间：2024-10-14 09:08:03.860685918 +0800
变更时间：2024-10-14 09:08:03.860685918 +0800
创建时间：2024-10-14 09:08:03.860685918 +0800
```

1. https://www.cnblogs.com/Gsealy/p/14480365.html
2. https://blog.csdn.net/DLW__/article/details/135648683

## 14.3 Linux 的长时数值模拟

借助 `screen` 工具，可以在断开连接后重新连接到会话。

- 新增会话：`screen`, `my_cmd &`
- 临时退出会话：`ctrl+a z`
- 列举会话：`screen -ls`
- 重连会话：`screen -r 1234`
- 杀死会话：`screen -S 1234 -X` 或 `ctrl+a k`
