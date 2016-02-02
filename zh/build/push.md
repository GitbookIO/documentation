# 用 GIT 更新书籍

当你的书是在 **gitbook.com** 上创建的, 你需要上传一些内容。要做到这一点, 您可以使用网页编辑器或者命令行.

如果你想使用命令行更新书籍, 你可以使用 [GIT](http://git-scm.com) 来上传内容:

### GIT Url

每一本书都与一个 Git HTTPS url 相关联. GitBook 的 Git 服务器目前还不支持 ssh协议.

git url 的格式是这样的:

```
https://git.gitbook.com/{{UserName}}/{{Book}}.git
```

### 授权

Git 服务器使用你的基本的 GitBook 登录信息进行身份验证. 当提示输入 GitBook 用户名和密码(你也可以使用API令牌).

### 保存你的凭证

为了避免每次上传内容都输入用户名和密码, 你可以向 `~/.netrc` 文件添加GitBook凭据. 你可以像下面这样创建或者向已存在的 `~/.netrc` 文件追加内容:

```
machine git.gitbook.com
  login USERNAME-or-EMAIL
  password API-TOKEN-or-PASSWORD
```

我们建议你使用 **API 令牌** 出于安全的原因, 你在这里可以发现它 [in your settings under "API"](https://www.gitbook.com/settings#api)

### 用命令行创建一个新的仓库

```
touch README.md SUMMARY.md
git init
git add README.md SUMMARY.md
git commit -m "first commit"
git remote add gitbook https://git.gitbook.com/{{UserName}}/{{Book}}.git
git push -u gitbook master
```

### 推送到 gitbook.com 已有仓库

```
git remote add gitbook https://git.gitbook.com/{{UserName}}/{{Book}}.git
git push -u gitbook master
```
