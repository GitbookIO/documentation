# 自定义域名

在 **Gitbook.com** 上所有的书籍都以 `http://{author}.gitbooks.io/{book}/` 的形式, 书籍的内容都可以通过访问 `http://{author}.gitbooks.io/{book}/content/` 获得.

但是你可以配置你的书籍来使用一个自定义的域名(GitBook 的免费功能). 域名可以用于你的个人主页或者内容(或者两者都使用).

添加一个自定义域名很容易.

### 在 GitBook.com 官网

在你书籍的 **Settings** 页面点击 **Domains**. 然后输入你的域名保存即可.

![在设置页面添加域名](../assets/add_domain.png)

### 域名注册商

完成上面操作之后你需要在域名注册商处做些操作:

1. 登录到你的域名注册商,找到可以允许你添加/编辑主机记录的页面. 这个页面一般在你的设置页面 `编辑 DNS`, `主机记录` 或者 `Zone File Control`.

2. 设置一条 **CNAME** 记录的 `www` 域名然后指向: ```www.gitbooks.io```.

3. 为了**重定向** 裸域名 (`yourdomain.com`) 到 `www.yourdomain.com`, 你需要开启 *"域名转发""*. 一般这个设置可以在这里找到: '转发', 'URL 转发' 或者 'URL 重定向'.


完成 ! DNS 解析可能还需要几个小时.
