+++
title = 'Ch19-开箱即用的 Octave/Matlab'
date = 2024-05-26T23:35:19+08:00
draft = false
tags = ["Windows", "Octave", "Matlab"]
categories = ["学习"]
+++

## 19.1 Octave

相比于 Python、R、Fortran、Julia 等科学计算编程语言，Octave 是类 Matlab 的开源的、开箱即用的科学计算工具。

```sh
pacman -Ss octave
pacman -S mingw64/mingw-w64-x86_64-octave
octave
plot(linspace(1,10))
exit
```

注：Windows 环境下 Octave 生成 SVG 图像存在问题。

## 19.2 Matlab

Matlab 是商业的科学计算工具，提供了更多、更稳健的工具箱和功能。

```sh
matlab -nodesktop   # 无 GUI 模式，非常好用
```
