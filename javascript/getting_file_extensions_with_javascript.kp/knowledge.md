---
title: What is the syntax for retrieving file extensions using javascript?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: You can get file extensions with JavaScript by using the String.prototype.split() method.
---

**Contents**

[TOC]

# Using Path Module

The Path module, part of the Node.js core API, provides several methods for working with file paths. One of these methods is `Path.extname()`, which returns the extension of the path, from the last occurrence of the . (period) character to the end of the string in the last portion of the path. 

Syntax:
`path.extname(path)`

Example:

```
const path = require('path');

console.log(path.extname('index.html'));
// Output: '.html'
```

# Using Regular Expressions

Regular expressions can also be used to get the file extension from a file path. For example, the following code uses a regular expression to get the extension of a file path:

```
const filePath = 'index.html';

const fileExtension = filePath.match(/\.([^.]+)$/)[1];

console.log(fileExtension);
// Output: 'html'
```
