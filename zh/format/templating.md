# 模板

这是 GitBook 可用的模板功能的预览. GitBook 使用 [Nunjucks](https://mozilla.github.io/nunjucks/) 和 [Jinja2](http://jinja.pocoo.org/) 两个模板引擎的语法.

### 转义

如果你想输出一些特殊的模板标签, 你可以使用原生的并且任何转义包含的内容都会被当作纯文本输出.

```
{% raw %}
  this will {{ not be processed }}
{% endraw %}
```

### 变量

一个变量从书籍的上下文中查找变量值.

变量被定义在 `book.json` 文件中:

```json
{
    "variables": {
        "myVariable": "Hello World"
    }
}
```


#### 显示变量

定义在 `book.json` 的变量可以在整本书的范围内访问:

```
{{ book.myVariable }}
```

以上会从 `book.json` 查找变量并显示变量值. 查找属性的变量名可以存在 `.` . 你也可以使用方括号语法.

```
{{ book.foo.bar }}
{{ book["bar"] }}
```

如果变量未定义, 那么什么都不会显示. 下面这些在 `foo` 未被定义的情况下不会产生任何输出: `{{ foo }}`, `{{ foo.bar }}`, `{{ foo.bar.baz }}`.


#### 上下文变量

通过一些变量可以获取一些关于当前文件或者书籍的信息:

| Name | Description |
| ---- | ----------- |
| `file.path` | 文件的相对路径 |
| `file.mtime` |文件的最后修改日期 |


### 标签

标签是在一些模版引擎上执行特殊操作的代码块.

#### If

**if** 标签测试一个条件让你可以有选择性地显示内容. 它起的作用跟在编程语言中一样.

````
{% if variable %}
  It is true
{% endif %}
```

如果变量 `variable` 被定义了并且值是true, 那么 "It is true" 将会被显示. 否则, 什么都不显示.

你可以使用 `elif` 和 `else` 来定义交叉的条件语句:

```
{% if hungry %}
  I am hungry
{% elif tired %}
  I am tired
{% else %}
  I am good!
{% endif %}
```

#### for

**for** 标签会迭代数组和字典.

让我们考虑在 `book.json` 文件中的变量:
```
{
    "variables": {
        "authors": [
            { "name": "Samy" },
            { "name": "Aaron" }
        ]
    }
}
```

```
# Authors


{% for author in book.authors %}
  - {{ author.name }}
{% endfor %}
```

上面的例子会列出在 `authors` 数组中使用 `name` 属性的每一个条目并且显示它们的值.

#### include

Include 标签详见 [内容引用](./conrefs.md) 这篇文章.
