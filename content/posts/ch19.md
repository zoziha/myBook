+++
title = 'ch19-开箱即用的 Octave'
date = 2024-05-26T23:35:19+08:00
draft = false
+++

相比于 Python、R、Fortran、Julia 等科学计算编程语言，Octave 是类 Matlab 的开源的、开箱即用的科学计算工具。

```sh
pacman -Ss octave
pacman -S mingw64/mingw-w64-x86_64-octave
octave
plot(linspace(1,10))
exit
```

注：Windows 环境下 Octave 生成 SVG 图像存在问题。
