# Math & TeX

因为一些插件 GitBook 支持数学公式和 TeX . 当前有两个支持数学公式的官方插件: [mathjax](https://github.com/GitbookIO/plugin-mathjax) 和 [katex](https://github.com/GitbookIO/plugin-katex).

#### 使用数学插件:

为了能够支持数学公式, 你需要添加一个插件到你书籍的 `book.json` 文件中:

```js
{
    "plugins": ["mathjax"]
}
```

#### MathJax 和 KaTeX 插件的区别

`mathjax` 和 `katex` 插件对 TeX 方程的展示用了不同的实现方式, 它们都有支持自己的开源代码库: [KaTeX](https://github.com/Khan/KaTeX) 和 [MathJax](https://www.mathjax.org).

MathJax 支持所有的 TeX 语法, 但是它在电子书(PDF, ePub 和 Mobi) 上的输出并不完美.
KaTeX 在所有的格式(web 和 ebooks)上表现地都很完美, 但是并不是所有的语法都支持 [所有语法](https://github.com/Khan/KaTeX/wiki/Function-Support-in-KaTeX).


#### 在内容中添加数学公式:

```
这里是一些行内的数学公式: $$a \ne 0$$
```

数学块应该新起一行:

```
这里是数学块:

$$
a \ne 0
$$
```