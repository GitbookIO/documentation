# AsciiDoc

从版本 `2.0.0` 开始, GitBook 也可以接受 AsciiDoc 作为一种输入格式.

请查阅 [AsciiDoc 语法快速指南](http://asciidoctor.org/docs/asciidoc-syntax-quick-reference/) 查看更多信息.

像 Markdown一样, GitBook 也在使用一些特殊的文件来组织结构: `README.adoc`, `SUMMARY.adoc`, `LANGS.adoc` and `GLOSSARY.adoc`.

### README.adoc

这是一本书的入口: 简介. 书籍入口文件必须是 `README.adoc`.

### SUMMARY.adoc

这个文件定义书籍的章节. 就像 [for markdown](./chapters.md), `SUMMARY.adoc` 文件的格式是一个简单的链接列表, 链接名用于章的名字, 链接目标指向该章文件所在的路径.

节的定义通向父章添加列表实现.

```
= Summary

. link:chapter-1/README.adoc[Chapter 1]
.. link:chapter-1/ARTICLE1.adoc[Article 1]
.. link:chapter-1/ARTICLE2.adoc[Article 2]
... link:chapter-1/ARTICLE-1-2-1.adoc[Article 1.2.1]
. link:chapter-2/README.adoc[Chapter 2]
. link:chapter-3/README.adoc[Chapter 3]
. link:chapter-4/README.adoc[Chapter 4]
.. Unfinished article
. Unfinished Chapter
```

### LANGS.adoc

针对 [多种语言的](./languages.md) 书籍, 这个文件可以用来定义书籍支持的不同语言和翻译.

这个文件的语法跟 `SUMMARY.adoc` 类似:

```
= Languages

. link:en/[English]
. link:fr/[French]
```

### GLOSSARY.adoc

这个文件是用于定义术语. [见术语表一章](./glossary.md).

```
= 术语表

== Magic
Sufficiently advanced technology, beyond the understanding of the observer producing a sense of wonder.

== PHP
An atrocious language, invented for the sole purpose of inflicting pain and suffering amongst the programming wizards of this world.
```



