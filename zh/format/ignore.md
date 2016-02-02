# 忽略文件和文件夹

GitBook 读取 `.gitignore`, `.bookignore` 和 `.ignore` 文件来获得需要忽略的文件和文件夹列表.

忽略文件的格式与 `.gitignore`文件相同:

```
# 这里是注释

# 忽略文件 test.md
test.md

# 忽略 "bin" 目录下的所有文件
bin/*
```