+++
title = 'Ch30-PowerShell 传递命令行参数'
date = 2024-05-26T23:35:19+08:00
draft = false
+++

当运行需要向运行环境传递自定义参数时，PowerShell 的命令行参数传递十分有用。示例：

```powershell
# 先决条件 `meson compile -C build` 生成可执行文件 FNL.exe
# 用法: `.\run_example.ps1 -NT 3` 设置线程数为 3
param(
    [Parameter()]
    [Int16]$NT = 3
)

write-host "Setting OMP_NUM_THREADS = $NT"
Write-Host "Running example A14W040 for FNL.exe"
$env:OMP_NUM_THREADS = $NT
.\build\FNL.exe -C .\example\A14W040
```

## 30.1 参考链接

1. [在 Windows PowerShell 中获取命令行参数](https://www.delftstack.com/zh/howto/powershell/command-line-arguments-in-powershell/)
