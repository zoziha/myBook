+++
title = 'ch37-Windows 资源管理与 Rust 高效应用集'
date = 2024-05-26T23:35:19+08:00
draft = false
+++

Windows 默认的资源管理器比较卡顿臃肿，使用 Rust 编写的 [Bottom][1] 轻量高效。通过 MSYS2 中 `pacman -S ucrt64/mingw-w64-ucrt-x86_64-bottom`
可以安装 Bottom，并在终端中使用 `btm -b` 命令，非常适合软件开发者。

[1]: https://clementtsang.github.io/bottom/0.9.6/

基于 Rust 编写的其它高效应用有：

1. [mdBook](https://github.com/rust-lang/mdBook)；
2. [starship](https://github.com/starship/starship)；
3. [bat](https://github.com/sharkdp/bat)；
4. [dust](https://github.com/bootandy/dust)；
5. [fd](https://github.com/sharkdp/fd)；
6. [hyperfine](https://github.com/sharkdp/hyperfine)。
