# 配置

所有的配置信息都以 JSON 的形式写在 `book.json` 文件中.

你可以将你 `book.json` 文件中的 JSON 粘贴到网站 [jsonlint.com](http://jsonlint.com) 来验证 JSON 的格式是否正确.

所有的字段都是可选的或者存在默认值.


## 字段

#### gitbook

```js
{ "gitbook": "2.x.x" }
```

此选项用于检测将使用哪个版本的 GitBook 来生成书. 格式符合 [SEMVER](http://semver.org) 规范.

#### title

```js
{ "title": "My Awesome Book" }
```

这个选项定义你书籍的标题, 默认情况下该值从 **README** 读取(第一个标题).

在网站 **gitbook.com**, 它的值为进入的平台的标题.

#### description

```js
{ "description": "This is such a great book!" }
```

这个选项定义你书籍的描述信息, 默认情况下该值从 **README** 读取(第一段).

在网站 **gitbook.com**, 它的值为进入的平台的描述信息.

#### isbn

```js
{ "isbn": "978-3-16-148410-0" }
```

这个选项定义你书籍的 ISBN（国际标准书号).  

#### language

```js
{ "language": "fr" }
```

这个选项定义书籍的语言, 默认值是 `en`.

此选项用于国际化和本地化, 它会改变网站的内容.

在网站 **gitbook.com**, 这个值为内容中指定的语言或者配置中设置的语言.

#### direction

```js
{ "direction": "rtl" }
```

这个属性将会设置语言的文本方向(译者注：比如内容从右往左流动).
建议设置 `language` 字段属性设置为正确文本方向相反的属性.

#### styles

这个选项用于向你的书籍中添加自定义css.

例如:

```js
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

#### plugins

```js
{ "plugins": ["mathjax"] }
```

一本书使用的插件列表定义在 `book.json` 文件中.

#### pluginsConfig

```js
{
    "plugins": ["myplugin"],
    "pluginsConfig": {
        "myPlugin": {
            "message": "Hello World"
        }
    }
}
```

这个选项包含所有插件的具体配置.

#### structure

这个选项用于覆盖被 GitBook 使用了的文件的路径.

比如你想用 `INTRO.md` 文件代替`README.md` 文件:

```js
{
    "structure": {
        "readme": "INTRO.md"
    }
}
```

这些结构类型的文件是 `readme`, `langs`, `summary` 和 `glossary`.

#### variables

```js
{
    "variables": {
        "myTest": "Hello World"
    }
}
```

这个选项定义将会在 [templating](./templating.md) 使用的变量的值.

#### pdf

PDF选项允许定制特定的页眉、页脚等.

```js
{
    "pdf": {
        "headerTemplate": "Header of the PDF with _TITLE_",
        "footerTemplate": "Footer HTML template. Available variables: _PAGENUM_, _TITLE_, _AUTHOR_ and _SECTION_."
    }
}
```
