+++
title = 'ch35-5 分钟教你在 Windows 上运行 Fortran'
date = 2024-05-26T23:35:19+08:00
draft = false
+++

> 📌5 分钟教你在 Windows 上运行 Fortran 。

> zoziha，e-mail: [zuo.zhihua@qq.com](mailto:zuo.zhihua@qq.com "zuo.zhihua@qq.com")，青岛黄岛，中铁世博城，2022-11-24。

## ⚙️环境搭建

从以下链接下载并安装 [msys2](https://mirrors.tuna.tsinghua.edu.cn/msys2/distrib/x86_64/ "msys2")：

```sh
https://mirrors.tuna.tsinghua.edu.cn/msys2/distrib/x86_64/    # 清华源
https://www.msys2.org/                                        # msys2 官网
```

同时按下 `Win+x+Shift+i` 键，打开 `powershell` ，输入以下命令，临时使用环境变量和安装 [编译器](https://gcc.gnu.org/ "编译器") [gfortran](https://gcc.gnu.org/ "gfortran") 和 [包管理器](https://fpm.fortran-lang.org/zh_CN/index.html "包管理器") [fpm](https://fpm.fortran-lang.org/zh_CN/index.html "fpm")：

```powershell
$env:path+=";C:\msys64\ucrt64\bin\;C:\msys64\usr\bin\"                  # 添加环境变量
pacman -S mingw-w64-ucrt-x86_64-gcc-fortran mingw-w64-ucrt-x86_64-fpm   # 安装编译器
```

输入 `Y` 回车确定，此时你已渐入佳境。

## ⚔️构建代码

输入以下命令，新建 [Fortran](https://fortran-lang.org/zh_CN/index "Fortran") 项目：

```sh
fpm new --app demo; cd demo               # 新建项目并切换路径
```

输入以下命令，打开记事本查看代码：

```sh
notepad app/main.f90                      # 使用记事本打开文件
```

```fortran
program main
  implicit none

  print *, "hello from project demo"         ! 打印语句
end program main
```

这是一个 `Fortran` 的主程序，关闭记事本，此时你已逐渐超神。

## 🚀运行程序

输入以下命令，编译运行程序：

```sh
fpm run                                   # 运行项目
```

```sh
 + mkdir build\dependencies
main.f90                               done.
demo.exe                               done.
[100%] Project compiled successfully.
 hello from project demo                    # 正确打印语句
```

好了，5 分钟，你已经超越了 50% 的 `Fortran` 用户了。学一下[**变量声明**](https://fortran-lang.org/zh_CN/learn/quickstart/variables/ "变量声明")**、**[**函数调用**](https://fortran-lang.org/zh_CN/learn/quickstart/organising_code/ "函数调用")**、**[**if**](https://fortran-lang.org/zh_CN/learn/quickstart/operators_control_flow/ "if")[**判断和**](https://fortran-lang.org/zh_CN/learn/quickstart/operators_control_flow/ "判断和")[**do**](https://fortran-lang.org/zh_CN/learn/quickstart/operators_control_flow/ "do")[**循环**](https://fortran-lang.org/zh_CN/learn/quickstart/operators_control_flow/ "循环")**、**[**数组及并行**](https://fortran-lang.org/zh_CN/learn/quickstart/arrays_strings/ "数组及并行")**、文件读写**，你会变得多强，我连想都不敢想😵！

> 备注：想要了解添加系统环境变量，去问一下必应或者 [Kimi AI](https://kimi.moonshot.cn/) 。

## 📺视频链接

<https://www.bilibili.com/video/BV1jg411i7iU/?vd_source=a399c2829da634847ecb0bca1d558517>

## ⏳远程协助

- 作者提供远程协助服务与 3 个月售后，价格：15元/次。
