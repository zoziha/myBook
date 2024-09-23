+++
title = 'Ch06-mdBook 与 Hugo'
date = 2024-05-26T23:35:19+08:00
lastmod = 2024-06-04T18:37:52+08:00
draft = false
tags = ["Windows", "Hugo"]
categories = ["计算机科学"]
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

## 6.1 `Hugo::LoveIt` 支持中文搜索

`LoveIt` 自带的2个搜索插件中文支持差，可以在网页项目中添加 `hugo-search-fuse-js` 来支持中文，`fuse.js` 主要读取摘要，为此：

1. 使用 `Hugo` Extend 版本；
2. 使用 `go.mod` 管理 `hugo mod get` 依赖；
3. 参考以下链接。

**参考链接：**
1. [使用Hugo搭建个人网站(二)-LoveIt主题自定义搜索](https://dnwzlx.com/posts/98850c88/#%E4%BF%AE%E6%94%B9%E6%90%9C%E7%B4%A2%E9%A1%B5%E9%9D%A2%E7%9A%84%E6%A0%B7%E5%BC%8F)；
2. [zoziha/mybook](https://github.com/zoziha/mybook)。
