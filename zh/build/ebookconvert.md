### 安装 ebook-convert

生成电子书 (epub, mobi, pdf) 需要 ebook-convert 组件i.

#### Mac

下载 [Calibre app](http://calibre-ebook.com/download). 在移动 `calibre.app` 到你的 Applications 目录下之后创建一个符号链接到 `ebook-convert` 工具:

```
$ sudo ln -s ~/Applications/calibre.app/Contents/MacOS/ebook-convert /usr/bin
```

你可以用你自己的 `$PATH` 所在的目录替换 `/usr/bin` .