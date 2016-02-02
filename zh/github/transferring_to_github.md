# 将内容转移到 GitHub

如果你先在 GitBook 书写你的书籍然后你现在想要将源文托管在 GitHub 上, 不用担心, 很简单就能实现.

#### 使用 GitHub 导入工具

1. 使用 GitHub **导入工具**:  [import.github.com/new](https://import.github.com/new)
2. 使用你的 GitBook git url, 例如: `https://git.gitbook.com/MyName/MyBook.git` (这个 url 可以在你书籍的设置中看到).
3. 为你的 GitHub 仓库输入一个名字.
4. 当提示认证的时候输入你的 GitBook 凭证 (你可以使用你的 API 令牌替代密码).
5. 完成!

当你的内容迁移到 GitHub 之后, 你现在可以设置集成功能这样 GitBook 就可以从 GitHub 同步内容: [GitHub 集成](./README.md)


#### 使用命令行

在GitHub 上创建一个仓库.

**注意:** 这个操作会重写你的 Git 仓库的历史this operation will overwrite your git history.

```
# clone 你的 GitBook 仓库 (你将需要输入用户名和密码)
$ git clone https://git.gitbook.com/MyName/MyBook.git ./mybook

# 进入克隆下书籍的根目录
cd ./mybook

# 推送到 Github
$ git push https://github.com/username/repo.git master --force
```