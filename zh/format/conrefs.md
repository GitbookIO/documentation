# 内容引用

内容引用(conref)是一种方便的机制以便重用其他书籍或者文件的内容.

### 导入本地文件

使用 `include` 标签可以轻易地导入另一个文件的内容:

```
{% include "./test.md" %}
```

### 从其他书籍导入文件

GitBook 可以处理使用使用 git 的包含路径:

```
{% include "git+https://github.com/GitbookIO/documentation.git/README.md#0.0.1" %}
```

git url 的格式是:

```
git+https://user@hostname/project/blah.git/file#commit-ish
```

正确的 git url 的路径应该以 `.git` 结束, 用来导入的文件名是从 `.git` 之后的剩下的 url 片段提取出来的.

`commit-ish` 可以是 任何标签, 哈希值, 或者可以检出的分支. 默认是 `master` 分支.

### 继承

模板继承是一种更容易重用模板的方式. 当编写一个模版时, 你可以定义子模版可以重载的 "blocks" . 继承链可以任意长, 只有你喜欢.

`block` 定义了模版上的某一部分并用名字标示它们. 父模版可以定义 "blocks" 然后子模版可以用心的内容覆盖它们.

```
{% extends "./mypage.md" %}

{% block pageContent %}
# 这是我的页面的内容
{% endblock %}
```

在文件 `mypage.md` 中, 你应该定义块的范围:

```
{% block pageContent %}
这是默认的内容
{% endblock %}

# License

{% import "./LICENSE" %}
```
