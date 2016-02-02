# Importing documents

Importing an existing document to GitBook is easy. Upload it when creating a book using the `Import` tab.

### Accepted formats

| Type | Extension |
| ---- | --------- |
| Microsoft Word Document | `.docx` |
| DocBook v5.x | `.xml` |
| HTML file | `.html` |

To use this feature as its most, we recommend using:
* Microsoft Word 2007+ documents
* DocBook v5.x documents

If you have existing DocBook documents in version 4, consider [converting it automatically](http://doccookbook.sourceforge.net/html/en/dbc.structure.db4-to-db5.html) to version 5 for optimized compatibility.

### Conversion

The import feature uses the [gitbook-convert](https://github.com/GitbookIO/gitbook-convert) CLI utility. This module is in charge of every aspect of the conversion of the original document to markdown files, along with the creation of the `SUMMARY.md`.

[gitbook-convert](https://github.com/GitbookIO/gitbook-convert) divide a big document into chapters and sub-chapters, based on the document's structure. Thus, each first-level header of the original document will be converted to a chapter. If a chapter contains second-level headers, a folder instead of a new file is created for this chapter. This folder will contain each sub-chapters.

In a chapter's folder, a `README.md` file containing the chapter preface is created. The whole content before the first second-level header is considered to be a chapter preface. The same rule applies for the whole content before the first first-level header which is used as the book's preface.

For `.docx` documents, [gitbook-convert](https://github.com/GitbookIO/gitbook-convert) will also export all included images into the `assets/` folder.

If you ever need more flexibility, consider using [gitbook-convert](https://github.com/GitbookIO/gitbook-convert) locally, create a repository and import it using Git or GitHub.

### Troubleshooting

We're always happy to help out with your books or any other questions you might have. You can ask a question or signal an issue on the following form at [github.com/GitbookIO/gitbook-convert](https://github.com/GitbookIO/gitbook-convert/issues).
