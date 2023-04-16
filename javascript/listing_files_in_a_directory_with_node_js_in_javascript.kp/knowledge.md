---
title: What is the syntax for retrieving a list of all file names in a directory using node.js?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: You can use the fs.readdir() function to get a list of the names of all files present in a directory in Node.js.
---

**Contents**

[TOC]

### Using the fs.readdirSync() Method

The `fs.readdirSync()` method can be used to get a list of the names of all files present in a directory in Node.js. This method takes the path of the directory as an argument and returns an array of the names of all files in the directory.

```javascript
const fs = require('fs');

const files = fs.readdirSync('/path/to/directory');

console.log(files); // ['file1.txt', 'file2.txt', 'file3.txt']
```

### Using the fs.readdir() Method

The `fs.readdir()` method can also be used to get a list of the names of all files present in a directory in Node.js. This method also takes the path of the directory as an argument, but returns a promise which resolves with an array of the names of all files in the directory.

```javascript
const fs = require('fs');

fs.readdir('/path/to/directory')
  .then(files => {
    console.log(files); // ['file1.txt', 'file2.txt', 'file3.txt']
  });
```
