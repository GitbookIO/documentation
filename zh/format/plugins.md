# 插件

使用插件是扩展 GitBook 功能的最好的方法 (ebook 和 website). 这里存在一些可以做很多事情的插件: 显示支持数学公式, 使用谷歌分析等, ...

### 如何查找插件?

可以在这里搜索插件 [plugins.gitbook.com](http://plugins.gitbook.com).

### 如何安装一个插件?

一旦你找到一个你想要安装的插件, 你需要把它添加到你书籍的 `book.json` 文件中:

```
{
	"plugins": ["myPlugin", "anotherPlugin"]
}
```

你也可以指定一个特定的版本: `"myPlugin@0.3.1"`, 指定版本是有用的, 特别是当你使用一个 GitBook 的过时的版本时.

如果你在本地构建你的书籍, 下载并准备插件只需简单地运行: `gitbook install`.



