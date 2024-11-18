+++
title = 'Ch37-Windows 资源管理与 Rust 高效应用集'
date = 2024-05-26T23:35:19+08:00
draft = false
categories = ["计算机科学"]
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

## 37.1 腾讯系扫盘问题

腾讯的软件如微信、START 云游戏存在频繁读取磁盘的现象，Windows 给的权限真的太宽了。
使用火绒进行自定义规则，禁止一些读写操作：

```sh
# WeChat
C:\Users\<USER_NAME>\AppData\Roaming\Tencent\WeChat\log\*
C:\Users\<USER_NAME>\Documents\WeChat Files\<USE_NAME>\config\*
C:\Users\<USER_NAME>\Documents\WeChat Files\All Users\config\*
# START
C:\Program Files\*
C:\*.sys
C:\WINDOWS\*.exe
D:\*
```

## 37.2 删除失效的默认打开程序条目

打开注册表 `计算机\HKEY_CLASSES_ROOT\Applications`，删除不需要的条目。
