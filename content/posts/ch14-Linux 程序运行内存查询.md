+++
title = 'Ch14-Linux 程序运行内存查询'
date = 2024-05-26T23:35:19+08:00
draft = false
+++

科学计算程序编程时可能需要查询程序运行时的内存使用情况。

```sh
ps -aux|grep benCh3d-grid2  # 查看 benCh3d-grid2 进程的 PID
cat /proc/3300706/status    # 查看 PID 为 3300706 的进程的内存使用
```

## 搭建 WSL-Debian 环境

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
