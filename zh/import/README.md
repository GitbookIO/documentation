# 导入文档

将已存在的文档导入到 GitBook 很容易. 当创建书籍的时候用 `Import` 选项上传要导入的文档即可.

### 支持的格式

| 类型 | 扩展名 |
| ---- | --------- |
| Microsoft Word Document | `.docx` |
| DocBook v5.x | `.xml` |
| HTML file | `.html` |

为了更好地使用这个功能, 我们推荐使用:
* Microsoft Word 2007+ documents
* DocBook v5.x documents

如果你现有的 DocBook 文档版本为 4, 考虑 [自动转换](http://doccookbook.sourceforge.net/html/en/dbc.structure.db4-to-db5.html) 到 5 为了兼容性.

### 转换

导入功能使用 [gitbook-convert](https://github.com/GitbookIO/gitbook-convert) CLI 程序. 这个模块负责原始文档到 markdown 文件转换的方方面面, 连同 `SUMMARY.md` 文件的创建.

[gitbook-convert](https://github.com/GitbookIO/gitbook-convert) 基于文档的结构, 将一个大的文档分割成章节和子章节. 因此, 原始文档的一级标题将会被转换成一个章. 如果一章包含二级标题, 将会为这章创建一个文件夹而不是新的文件. 这个文件夹将会包含每个子章节.

在章节的文件夹, 一个包含章节序言的 `README.md` 文件默认被创建. 在第一个二级标题之前的所有内容都被视为章节序言. 同样的规则也适用第一个标题之前的所有内容, 该内容为书籍的序言.

对于 `.docx` 文档, [gitbook-convert](https://github.com/GitbookIO/gitbook-convert) 也会将所有的图片导出到 `assets/` 文件夹下.

如果你需要更大的灵活性, 可以考虑在本地使用 [gitbook-convert](https://github.com/GitbookIO/gitbook-convert) , 创建一个仓库然后用 Git 或者 GitHub 导入 [gitbook-convert](https://github.com/GitbookIO/gitbook-convert).

### 故障排除

我们总是乐于帮助你的书或者其他任何你可能遇到的问题. 你可以问一个问题或者在下面的地址创建一个 issue : [github.com/GitbookIO/gitbook-convert](https://github.com/GitbookIO/gitbook-convert/issues).
