# 章节

GitBook 使用一个 `SUMMARY.md` 文件来定义书籍的章节结构.  `SUMMARY.md` 文件通常用于生成书籍的目录表.

文件 `SUMMARY.md` 的格式是一个简单的链接列表, 链接的名称用作该章的名称, 链接的目标是该章对应的文件的路径.

通过向章添加简单的嵌套表定义每章小节的结构.

### 简例

```
# 章节结构

* [chapter 1](chapter1.md)
* [chapter 2](chapter2.md)
* [chapter 3](chapter3.md)
```

### 节分为不同部分的例子

```
# 章节结构

* [Part I](part1/README.md)
    * [Writing is nice](part1/writing.md)
    * [GitBook is nice](part1/gitbook.md)
* [Part II](part2/README.md)
    * [We love feedback](part2/feedback_please.md)
    * [Better tools for authors](part2/better_tools.md)
```

