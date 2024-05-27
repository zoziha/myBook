+++
title = 'Ch06-mdBook 与 Hugo'
date = 2024-05-26T23:35:19+08:00
draft = false
tags = ["Windows"]
categories = ["娱乐"]
+++

[`mdBook`][1] 借助 [markdown][2] 创建静态图书网页。
[`Hugo`][3] 借助 [markdown][2] 创建动态博客网页，本博客采用 [LoveIt][4] 主题。

[1]: https://github.com/rust-lang/mdBook
[2]: https://markdown.com.cn/
[3]: https://www.gohugo.org/doc/
[4]: https://hugoloveit.com/zh-cn/

```sh
mdbook build
hugo new posts/my-first-post.md
hugo server -D
```
