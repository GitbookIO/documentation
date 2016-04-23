# Builds and History

After you pushed content using [**git** or the **editor**](./push.md), GitBook.com will start different builds:

- **website**: it will generate the website
- **json**: it will extract metadata about the book (summary, introduction, etc)
- **epub**: it will generate the epub download
- **pdf**: it will generate the pdf download

These builds are listed and detailed on the **History** tab of your book.

### Builds not triggered

If your book is linked to GitHub, it may happen that GitHub doesn't signal changes to GitBook (for example: if authorizations are reset).
Information on how to fix this issue is available on the [GitHub integration section](../github/README.md).

### Fixing build errors

If your build failed, you can use the logs to debug the issue and publish a fixed content.

[Read more about common build errors](./errors.md)
