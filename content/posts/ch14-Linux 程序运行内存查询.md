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
