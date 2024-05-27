+++
title = 'ch27-Fortran 编程'
date = 2024-05-26T23:35:19+08:00
draft = false
tags = ["Fortran"]
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
7. [Intel VTune Profiler](https://software.intel.com/content/www/us/en/develop/tools/vtune-profiler.html)。

{{< typeit code=Fortran >}}
program main
    print *, "Hello, world!"
end program main
{{< /typeit >}}

备注：[华为是为数不多的涉及高性能编译器的国内公司之一][3]。

[3]: https://support.huawei.com/enterprise/zh/doc/EDOC1100283328/8de2b49a
