+++
title = 'Ch27-Fortran 编程'
date = 2024-05-26T23:35:19+08:00
lastmod = 2024-06-04T18:37:52+08:00
draft = false
tags = ["Fortran", "MKL", "编程"]
categories = ["学习"]
+++

[Fortran][1] 是一种适应数学表达、高性能科学计算的成熟、免费语言，这是它的特色。

随着 [Fortran-lang 社区的努力][2]，Fortran 迎来复苏迹象，作者看好这种发展，虽然 Fortran 也存在一些问题：

1. [开源社区][3]生态小，开发者少；
2. 语法糖少，语言标准迭代缓慢且不一定具有流行性。

[1]: https://fortran-lang.org/zh_CN/learn/quickstart/
[2]: https://fortran-lang.discourse.group/t/fortran-returns-to-top-20-tiobe-index/1069/203?u=zoziha
[3]: https://github.com/fortran-lang

我常使用以下工具链软件：

1. [GNU Fortran](https://gcc.gnu.org/fortran/)；
2. [GDB](https://www.gnu.org/software/gdb/)；
3. [VS Code](https://code.visualstudio.com/)；
4. [Meson](https://mesonbuild.com/)；
5. [FORD](https://github.com/Fortran-FOSS-Programmers/ford)；
6. [Git](https://git-scm.com/)；
7. [Intel VTune Profiler](https://software.intel.com/content/www/us/en/develop/tools/vtune-profiler.html)；
8. [Intel oneAPI 组件](https://www.intel.cn/content/www/cn/zh/developer/articles/tool/oneapi-standalone-components.html#fortran)。

{{< typeit code=Fortran >}}
program main
    print *, "Hello, world!"
end program main
{{< /typeit >}}

备注：[华为是为数不多的涉及高性能编译器的国内公司之一][3]。

[3]: https://support.huawei.com/enterprise/zh/doc/EDOC1100283328/8de2b49a

## 27.1 fpm 与 meson

fpm 目前还不够成熟，主要表现在对外部链接的支持上，meson 则相对更成熟。

这是我写的[《Fortran中文手册》](https://gitee.com/zoziha/modern-fortran-chinese-manual/releases)。

### 27.1.1 Fpm-更适合小型代码

```sh
fpm new my_project
fpm run
```

### 27.1.2 Meson-更适合大型代码

使用 meson、CMake、GFortran 等工具，可以方便在远程服务器（Linux、Windows-MSYS2）上使用编译环境。

```sh
meson init --language=fortran --version=0.1.0 --build --name=myproject
meson setup build
meson compile -C build
meson devenv -C build
```

## 27.2 包复用的基础

1. 容易获取，如采用通用获取手段；
2. 社区官方持续支持；
3. 接口简单、文档健全。

## 27.3 Windows 下 使用 CMake 和 MSYS2-GFortran 链接 oneMKL

这类需求一般很少，我曾尝试为 Stdlib 链接 oneMKL ，只是记录下来。Windows 下其实是可以使用 GFortran 链接
oneMKL 的，原因是 oneMKL 中的 BLAS 是 C 接口或者 Fortran77 写的。

1. 首先，下载和启动 oneMKL 环境变量。
    ```powershell
    &"D:\Program Files (x86)\Intel\oneAPI\setvars.bat"
    ```
2. [设置 CMake 查询 MKL][4]。
    ```CMake
    find_package(MKL)
    target_link_libraries(${PROJECT_NAME} ${MKL_LIBRARIES})
    ```

[4]: https://cmake.org/cmake/help/latest/module/FindBLAS.html

## 27.4 Git 补丁使用

```sh
git diff > 1.patch  # 注意 PowerShell 可能会使用 UTF-16 编码
git apply 1.patch
```
