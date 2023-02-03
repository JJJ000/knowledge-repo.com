---
title: Remove html tags from text using javascript
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-03 00:00:00
updated_at: 2023-02-03 00:00:00
tldr: Use the String.prototype.replace() method to replace HTML tags with an empty string.
---

**Contents**

[TOC]

#### Regular Expressions

The following regular expression can be used to strip HTML from text in Javascript:

```
/<[^>]+>/g
```

This expression will match any HTML tag and remove it from the text.

#### Using a Library

Another option is to use a library such as [html-minifier](https://www.npmjs.com/package/html-minifier). This library can be used to minify HTML and remove any unnecessary tags and attributes.

#### Using a Function

You can also create a custom function to strip HTML from text. This function can be used to loop through the text and remove any HTML tags it finds.

```javascript
function stripHtml(text) {
  return text.replace(/<[^>]+>/g, '');
}
```

#### Using a Third-Party Service

Finally, you can use a third-party service such as [HTML Cleaner](https://html-cleaner.com/) to strip HTML from text. This service allows you to paste in HTML code and it will automatically remove any unnecessary tags and attributes.
