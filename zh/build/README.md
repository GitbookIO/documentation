# 构建和历史

当你使用 [**Git** 或者 **编辑器**](./push.md) 提交内容之后, GitBook.com 将会开始不同的构建:

- **website**: 它将会生成静态站点
- **json**: 它将会提取书籍的元素 (目录, 简介, 等等)
- **epub**: 它将会生成可下载的 epub 
- **pdf**: 它将会生成可下载的 pdf 

这些构建任务详细地列在你书籍的 **History** 选项.

### 构建不触发

如果你的书籍与 GitHub 关联, 可能发生 GitHub 与 GitBook 不同步的问题 (比如: 如果授权重置).
关于解决这个问题的更多信息请见 [GitHub integration section](../github/README.md).

### 解决构建错误

如果构建失败, 您可以使用日志来调试问题并发布解决方案.

[阅读更多关于构建的错误](./errors.md)
