# 扩展站点和电子书的风格

你可以通过在 `styles` 目录下创建 `.css` 文件来扩展电子书和网站的样式:

| 类型 | 文件 |
| ---- | ---- |
| `website` | `styles/website.css` |
| `pdf` | `styles/pdf.css` |
| `epub` | `styles/epub.css` |
| `mobi` | `styles/mobi.css` |
| `pdf`, `epub`, `mobi` | `styles/ebook.css` |


这些路径可以在 `book.json` 的配置中更改, 例如使用根目录下的文件:

```json
{
    "styles": {
        "website": "styles/website.css",
        "ebook": "styles/ebook.css",
        "pdf": "styles/pdf.css",
        "mobi": "styles/mobi.css",
        "epub": "styles/epub.css"
    }
}
```

#### 使用CSS预处理器

这里有一些让使用CSS预处理器更方便的插件:

- [styles-less](https://plugins.gitbook.com/plugin/styles-less)
- [styles-sass](https://plugins.gitbook.com/plugin/styles-sass)

