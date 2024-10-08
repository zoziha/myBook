+++
title = 'Ch46-Zotero使用Aminer存储PDF'
date = 2024-06-13T18:40:11+08:00
draft = false
tags = ["zotero", "Windows", "aminer", "Sumatrapdf"]
categories = ["计算机科学"]
+++

Zotero 是一款便捷的文献管理软件，但由于服务器负担，只提供普通用户 100Mb 的存储空间；
[Aminer][1] 是一个文献查找网站，可以附带 PDF 文档。可以借助 Aminer 托管 PDF，并在 Zotero 中备注网址。

Zotero 的 GB7714-2015 样式见[GB/T 7714—2015（顺序编码，双语，姓名不大写，无 URL、DOI，网络首发文献除外）][2]。

[1]: https://www.aminer.cn/
[2]: https://gitee.com/redleafnew00/Chinese-STD-GB-T-7714-related-csl/raw/main/src/gb-t-7714-2015-numeric-bilingual-no-uppercase-no-url-doi-except-aop/gb-t-7714-2015-numeric-bilingual-no-uppercase-no-url-doi-except-aop.csl

## 46.1 SumatraPDF 自定义按键

笔记本电脑一般没有 Page Up/Down 键，在使用笔记本阅读 pdf 文件时，就会窘迫。使用 SumatraPDF 可以输入 Return 或 Space 表示 Page Down，但是不够直观。或许可以通过自定义按键来形成个人习惯方案，打开高级选项，比如将 `<` 和 `>` 键绑定到 Page Up/Down 键：

```text
Shortcuts [
    [
        Cmd = CmdScrollUpPage
        Key = ,
    ]
    [
        Cmd = CmdScrollDownPage
        Key = .
    ]
]
```
