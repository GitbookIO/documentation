# Markdown

GitBook 默认使用 Markdown 的语法.

这是作为一个快速的参考和展示. 更多详细信息见 [John Gruber's original spec](http://daringfireball.net/projects/markdown/) 和 [Github-flavored Markdown info page](http://github.github.com/github-flavored-markdown/).


## 标题

```markdown
# H1
## H2
### H3
#### H4
##### H5
###### H6
```

另外, 对一级标题和二级标题, 下划线的样式：

```markdown
Alt-H1
======

Alt-H2
------
```

## 段落和换行符

一个段落是一个或多个连续的文本行, 由一个或多个空白行分隔. (这些空白行都视为一个空白行 —— 一行只包括空格或者制表符被认为是空白的.) 正常的段落不应留有空格或制表符.

```markdown
从这里开始一行.

这一行从上面开始被两个换行分开, 因此它是一个 *单独的段落*.

这一行也是一个单独的段落, 但是...
这一行只被一个单独的换行分开，因此它时 *同一段落* 的新一行.
```


## 强调

```markdown
强调, 又名斜体, 用 *星号* 或者 _下划线_.

特别强调, 又称加粗, 用 **两个星号** 或者 __两个下划线__.

两者结合可以用 **两个星号 和 _一个下划线_**.

删除线使用两个 `~` 符号. ~~删除这个~~
```

## 列表

(在这个例子中, 首尾空格用点表示: ⋅)

```markdown
1. 列表第一项
2. 另一项
⋅⋅* 无序子列表
1. 实际数字并不重要, 只是一个编号
⋅⋅1. 有序子列表
4. 另一项

⋅⋅⋅你可以在列表项中适当缩进段落. 注意上面的空行和空格 (至少有一个空行，但我们也可以在这里使用三个点达到同样的效果).

⋅⋅⋅新起一行而不新起一段, 你需要在上一行后面空两格然后回车.⋅⋅
⋅⋅⋅注意这一行是新起的一行, 但是和上一行在相同段落里.⋅⋅
⋅⋅⋅(这与典型的 GFM 换行符不同, 它的行后面不需要两个空格.)

* 无序列表可以使用星号
- 或者减号
+ 或者加号
```

## 链接

有两种方式创建链接.

```markdown
[我是一个行内式的链接](https://www.google.com)

[我是一个有标题的行内式的链接](https://www.google.com "Google's Homepage")

[我是一个参考式的链接][任意的不区分大小写的参考文本]

[我是一个指向仓库参考文件的引用](../blob/master/LICENSE)

[你可以使用数字定义的参考式链接][1]

或者创建一个无参考文本的链接(即只有[]没有()的链接), 像这样 [链接文本自身充当参考]

后文会展示一些参考链接.

[任意的不区分大小写的参考文本]: https://www.mozilla.org
[1]: http://slashdot.org
[链接文本自身充当参考]: http://www.reddit.com
```

## 脚注
Markdown默认使用的脚注链接并不会显示在页面上. 有时我们需要使用不包含超链接的脚注显示给读者. 针对无超链接的脚注, GitBook 提供像下面这样的简单的语法支持.

```markdown
Text prior to footnote reference.[^2]
[^2] Comment to include in footnote.
```

## 图片

```markdown
这是我们的 logo (鼠标移到图片上方查看标题文本):

行内式:
![图片不能显示时的替换文本](https://github.com/adam-p/markdown-here/raw/master/src/common/images/icon48.png "Logo 标题文本 1")

参考式:
![图片不能显示时的替换文本][logo]

[logo]: https://github.com/adam-p/markdown-here/raw/master/src/common/images/icon48.png "Logo 标题文本 2"
```

## 代码语法高亮显示

代码块石 Markdown 规范的一部分, 但语法高亮却不是. 然而许多网站 -- 像 Github 和 *Markdown Here* 的渲染器 -- 都支持语法高亮显示. 根据渲染器的不同, 支持的语言以及语言的书写方式可能都会有所不同. *Markdown Here* 支持数十种语言的高亮显示 (不仅仅是编程语言, 还有 diffs 和 HTTP headers); 查看详细的支持的编程语言列表以及如何书写他们名字, 参考这里 [highlight.js demo page](http://softwaremaniacs.org/media/soft/highlight/test.html).

```markdown
Inline `code` has `back-ticks around` it.
```

代码块前后各被三个反勾号 （<code>```</code>） 包围着, 或者缩进4个空格. 我推荐使用前者 -- 这种方式书写更容易并且只有这种方式才支持语法高亮.

<pre lang="no-highlight"><code>```javascript
var s = "JavaScript 语法高亮";
alert(s);
```

```python
s = "Python 语法高亮"
print s
```

```
没有声明语言, 所以没有语法高亮.
但是我们可以添加一个 &lt;b&gt;加黑标签&lt;/b&gt;.
```
</code></pre>

## 表格

表格也不是 Markdown 规范的核心部分, 但却是 GFM 的一部分, 并且 *Markdown Here* 也支持表格. 向你的电子邮件添加表格有很容易的方法 -- 一个需要从其他应用程序复制粘贴的功能.

```markdown
冒号用于调整列.

| Tables        | Are           | Cool  |
| ------------- |:-------------:| -----:|
| 第三列         | 右对齐         | $1600 |
| 第二列         | 居中      	 |   $12 |
| zebra stripes | are neat      |    $1 |

外面的竖线 (|) 是可选的, 你没必要向上面那样整齐地排列. 你也可以使用下面的方式:

Markdown | Less | Pretty
--- | --- | ---
*Still* | `renders` | **nicely**
1 | 2 | 3
```

## 引用

```markdown
> 回复电子邮件时使用引用很方便.
> 这一行处于同一个引用.

结束引用.

> 这行非常长但仍然被一个引用包着. 来来来来来来来来来来来来来来来来我们继续多写一点来确保这行足够长来确保能被引用完全包着. 对了, 你可以在引用内使用 **Markdown** 语法.
```

## 插入 HTML

你也可以插入 HTML 代码, 它们大多能支持地很好.

```markdown
<dl>
  <dt>Definition list</dt>
  <dd>Is something people use sometimes.</dd>

  <dt>Markdown in HTML</dt>
  <dd>Does *not* work **very** well. Use HTML <em>tags</em>.</dd>
</dl>
```


## 水平分割线

```markdown
三种或者更多种方式...

---

连字符

***

星号

___

下划线
```
