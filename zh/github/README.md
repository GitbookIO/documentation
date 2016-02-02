# GitHub 集成

GitBook 可以完美地集成 [GitHub](https://github.com) 并用后者托管你的书籍文件.

## 连接你的账号/权限

在连接你的书籍与 GitHub 之前, 你需要授权 GitBook 访问你的 GitHub 账户.

在你的 [账户设置](https://www.gitbook.com/settings), 连接你的 GitHub 账户需要正确的权限:

- **Default permissions**: 只在你登录的时候授权你访问 GitHub
- **Access to webhook**: 访问你的 GitHub 账户在你指定的仓库上创建一个 webhook (详见 [webhooks](#webhooks)).
- **Access to public repositories**: 访问你的 GitHub 的仓库 这样你就可以 更方便地从 GitBook 编辑你的书籍 (只针对公开的仓库)
- **Access to private repositories**: 和上面一样不过可以访问私有仓库

## 从 GitHub 导入一本书籍

当你创建一本新的书籍时, 通过 `GitHub` 选项卡你可以选择要导入的 GitHub 仓库.

新创建的书籍将被设置成你仓库的内容, 并且会自动添加一个 webhook.

## Webhooks

当你 GitHub 仓库的内容发生改变时, Webhooks 会通知 GitBook.

如果你 GitHub 仓库的更改没有同步到 GitBook, 那么问题的主要来源是 webhook. 你可以检查下你仓库设置里的 webhook 的状态.


## 建立书籍和仓库的连接

当你的 GitHub 账户正确地关联了你的 GitBook 帐户, 那么关联一本书到一个仓库就会很容易了.

**注意:** 当你在书籍的设置中制定一个 GitHub 仓库时, GitHub 仓库的优先级将会 GitBook 的仓库, 这意味着编辑器将会直接编辑 GitHub 上的内容, 然后同步到 GitBook.

**同步是单向的**, 仅仅是 GitHub 仓库内容的更改会触发 GitBook 仓库内容的同步, GitBook 仓库内容的更改 **不会** 更新你 GitHub 仓库之前写入的内容.

1. 打开你书籍设置中的 GitHub 部分
2. 输入你的仓库 id (例如: `你的GitHub账户名/仓库名`)
3. 保存设置
4. 点击按钮 **Add a deployment webhook**

你现在可以从 web 编辑器编辑你的 GitHub仓库了(如果你已经授予了正确的权限), 然后你在 GitHub 上的提交将会触发 GitBook 书籍的构建.

## 常见错误:

##### 我的书籍没有被更新 / 我没看到任何构建

如果你关联了 GitHub 仓库到 GitBook 但是 编辑内容并未触发 GitBook 的任何构建操作.
确认 webhook 被正确添加到了你的 GiitHub 仓库 (在你仓库的 settings -> Webhook). 如果 webhook 不存在或者无效, 那么将它添加回你书籍的设置中.

##### 书籍 名字/拥有者 的更改

如果你把书籍转让给了其他人, 那么 webhook 将会失效, 你需要重新把它添加回来.
