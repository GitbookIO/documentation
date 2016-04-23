# Transferring content to GitHub

If you started writing your book on GitBook and you now want to host its source on GitHub, don't worry, it's easy.

#### Using the GitHub Import Tool

1. Use the **Import Tool** from GitHub:  [import.github.com/new](https://import.github.com/new)
2. Enter your GitBook git url, for example: `https://git.gitbook.com/MyName/MyBook.git` (this url can be found in your book settings).
3. Enter a name for your GitHub repository.
4. Enter your GitBook credentials (you can use your API token instead of your password) when prompted.
5. Done!

When your content as been transferred to GitHub, you can now setup the integration so that GitBook can still build your book from GitHub: [GitHub Integration](./README.md)


#### Using the command line

After creating a repository on GitHub.

**Caution:** this operation will overwrite your git history.

```
# Clone your GitBook repository (you'll need to enter your username and password)
$ git clone https://git.gitbook.com/MyName/MyBook.git ./mybook

# Enter the cloned book
cd ./mybook

# Push it to Github
$ git push https://github.com/username/repo.git master --force
```