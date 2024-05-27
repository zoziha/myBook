+++
title = 'Ch26-VS Code 配置 Meson'
date = 2024-05-26T23:35:19+08:00
draft = false
+++

Windows 下通过 MSYS2 安装 [Meson][1]，VS Code 配置 Meson 涉及到：

* [`mesonlsp`][2]: Meson 的 LSP 服务器，用于提供语法高亮、自动补全等；
* [`muon`][3]: Meson 的 C99 实现，用于格式化代码（支持 Meson 语法或不及时）。

[1]: https://mesonbuild.com/
[2]: https://github.com/JCWasmx86/mesonlsp
[3]: https://github.com/annacrombie/muon
