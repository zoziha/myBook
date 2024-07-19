+++
title = 'Ch30-PowerShell 传递命令行参数'
date = 2024-05-26T23:35:19+08:00
draft = false
tags = ["Windows", "PowerShell", "OpenMP"]
categories = ["学习"]
+++

当运行需要向运行环境传递自定义参数时，[PowerShell 的命令行参数传递][1]十分有用。示例：

```powershell
# 先决条件 `meson compile -C build` 生成可执行文件 FNL.exe
# 用法: `.\tools\run_example.ps1 -NT 3 -Args "-C .\example\A14W040 -i"` 设置线程数为 3
param(
    [Parameter()]
    [Int16]$NT = 3,
    [String]$Args = "-C .\example\A14W040"
)

write-host "Setting " -NoNewline;
write-host "OMP_NUM_THREADS = $NT" -Foregroundcolor Green -NoNewline;
$env:OMP_NUM_THREADS = $NT

$App = ".\build\FNL.exe"
write-host ", running ""$App $Args"" ..."
Invoke-Expression -Command "$App $Args"
```

## 30.1 Windows 创建软链接

软链接可以方便在 PATH 路径中部署一些实用的命令行工具：

```cmd
mklink "C:\msys64\ucrt64\bin\Notepad4.exe"  "D:\Program Files\Notepad4\Notepad4.exe"
```

## 30.2 科学 `clash`

```powershell
# clash.ps1
# 临时添加代理，并且运行联网命令, 例如 `clash -Command "git push"`
param(
    [string]$Command = "echo $env:https_proxy"
)

& {
    $env:http_proxy = "http://127.0.0.1:7890"
    $env:https_proxy = "http://127.0.0.1:7890"

    # 执行命令
    Invoke-Expression -Command $Command
}
```

## 30.3 OMP 线程配置与计算

```powershell
# omp.ps1, run example: ./omp.ps1 -Command "./build/FNL -C example/case1" -NT 3
# 临时更改OMP_NUM_THREADS，并且运行计算命令
param(
    [int16]$NT = 4,
    [string]$Command = "echo $env:OMP_NUM_THREADS"
)

& {
    $env:OMP_NUM_THREADS = $NT

    # 执行计算命令
    Invoke-Expression -Command $Command
}
```

[1]: https://www.delftstack.com/zh/howto/powershell/command-line-arguments-in-powershell
