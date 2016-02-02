# 常见错误

这里列出了一些常见的构建错误和相关的解决方法.

---------

```
Error loading plugins: plugin1, ...
```

发生这个错误是因为 GitBook 不能识别一个插件 (或者插件是无效的).
扩展的插件需要提前用 `gitbook install` 安装.

一些插件不能被加载的原因也有可能是它需要其它版本的 GitBook. 如果是这种情况, 你可以找到支持你当前 GitBook 版本的正确版本的插件, 你可以这样在 `book.json` 定义:

```
{
    "plugins": ["myPlugin@1.2.3"]
}
```

---------

```
Need to install ebook-convert from Calibre
```


为了避免在你试图构建你的项目作为一个 PDF, ePub 或者手机域名的电子书时产生错误, 你必须安装 [Calibre](http://calibre-ebook.com) 电子书阅读器/管理器 _并且_ 安装命令行工具.

安装 Calibre Mac 版本的命令行工具, 从菜单中选择: **calibre - Preferences - Miscellaneous - Install command line tools**

一旦你完成这些操作, 你的电子书就会构建成功.

---------
