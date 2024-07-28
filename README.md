# 旅行者 `0x2` 号

* 仓库：https://gitee.com/zoziha/mybook ,
或 https://github.com/zoziha/mybook ；
* 网页：https://userzuo.netlify.app/ 。

[`hugo`](https://userzuo.netlify.app/ch06-mdbook-%E4%B8%8E-hugo/)
构建命令：

```sh
git clone --recurse-submodules https://github.com/zoziha/mybook
hugo server -D
hugo new posts/my-first-post.md
```

> [!IMPORTANT]
> 这是一个个人博客笔记，请勿使用。

## 文档撰写与网页发布

在 `content/posts` 目录下，撰写文档草稿，并提交文档到临时分支 `trunk`。
完成一定量的草稿提交，`trunk` 分支被合并到 `main` 分支。
将 `main` 所有提交推送到远程仓库，会触发 GitHub Actions 自动构建并发布网页到 `netlify`。
