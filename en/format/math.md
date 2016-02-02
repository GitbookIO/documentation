# Math & TeX

GitBook supports math equations and TeX thanks to plugins. There are currently 2 official plugins to display math: [mathjax](https://github.com/GitbookIO/plugin-mathjax) and [katex](https://github.com/GitbookIO/plugin-katex).

#### Enable a math plugin:

To enable math support, you need to add one of these plugins to your `book.json`:

```js
{
    "plugins": ["mathjax"]
}
```

#### Differences between MathJax and KaTeX

The `mathjax` and `katex` plugins are different implementations of TeX equation rendering, backed by their respective Open Source libraries: [KaTeX](https://github.com/Khan/KaTeX) and [MathJax](https://www.mathjax.org).

MathJax supports the entire TeX syntax, but the output is not perfect on ebooks (PDF, ePub and Mobi).
KaTeX renders perfectly on all formats (web and ebooks), but doesn't yet support [all the syntax](https://github.com/Khan/KaTeX/wiki/Function-Support-in-KaTeX).


#### Add math to your content:

```
Here is some inline math: $$a \ne 0$$
```

A block of math should begin with a new line:

```
Here is a block of math:

$$
a \ne 0
$$
```