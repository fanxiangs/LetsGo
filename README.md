# [Golang 视频教程](https://pegasuswang.github.io/LetsGo/)

![](./golang.png)

## 目的

通过连载短视频和文章的形式帮助有一定其他语言编程基础的人快速学习和入门 Golang。
内容包括 Golang 基础、内置库、web 开发、并发编程等，均来自笔者日常学习和开发经验总结。
教程中会有一些和 Python 等语言特性的对比，方便读者理解。希望教程有如下特色：

- 每一小节均包含视频和文章，演示笔者日常开发的工作流（当然未必是最佳方式，读者朋友可以分享下自己的开发经验）
- 全部代码视频中现场编写，避免教科书式枯燥讲解代码
- 主次分明，快速上手，主要分享日常业务开发中最常用的特性
- 结合实战，笔者自己边踩坑边总结业务开发中遇到的一些痛点和解决方案。比如如何做单测、代码如何分层、如何排查性能问题等
- 最佳实践。总结业务开发中一些好的实践分享出来，贴地气

主要面向有一定开发经验的开发者，不会涉及到一些非常具体和细节的问题。 比如如何下载 IDE，如何导出环境变量等，
编程新手可以先补一补开发基础。

阅读地址：[https://pegasuswang.github.io/LetsGo/](https://pegasuswang.github.io/LetsGo/)

## 如何快速上手新语言

笔者的经验就是『学以致用』，如果光学不练，很快就会忘记。学一门新语言的最好方式就是在熟悉了基本语法以后，
通过**大量**的编码和项目练习来熟悉它。期间你还需要频繁借助文档/搜索引擎等工具，边写边查，很快就可以上手。
之后再去考虑一些具体的语言细节和深入的特性，

## 工具

笔者使用 when-changed 来监控文件变动并且执行 go 代码，这样你可以边写代码，保存后自动运行观察结果，
在写代码验证你的想法的时候会比较方便，视频里笔者会详细演示。

```sh
pip install when-changed
when-changed -v -r -1 -s ./    go run main.go
```

## 本电子书制作和写作方式
使用 mkdocs 和 markdown 构建，使用 Python-Markdown-Math 完成数学公式。
markdown 语法参考：http://xianbai.me/learn-md/article/about/readme.html

安装依赖：

```sh
pip install mkdocs    # 制作电子书, http://markdown-docs-zh.readthedocs.io/zh_CN/latest/
# https://stackoverflow.com/questions/27882261/mkdocs-and-mathjax/31874157
pip install https://github.com/mitya57/python-markdown-math/archive/master.zip

# 或者直接
pip install -r requirements.txt

# 如果你 fork 了本项目，可以定期拉取主仓库的代码来获取更新，目前还在不断更新相关章节
```

你可以 clone 本项目后在本地编写和查看电子书：

```sh
mkdocs serve     # 修改自动更新，浏览器打开 http://localhost:8000 访问
# 数学公式参考 https://www.zybuluo.com/codeep/note/163962
mkdocs gh-deploy    # 部署到自己的 github pages
```
