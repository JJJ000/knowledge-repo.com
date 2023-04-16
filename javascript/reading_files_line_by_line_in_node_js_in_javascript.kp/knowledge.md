---
title: How can I read a file line by line in node.js?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: To read a file one line at a time in node.js, use the fs.readFileSync() method.
---

**Contents**

[TOC]

**Section 1: Setting up the File System**

The first step is to set up the file system that will be used to read the file. This can be done by requiring the 'fs' module and creating a variable that will hold the file path.

```javascript
const fs = require('fs');
const filePath = './file.txt';
```

**Section 2: Reading the File**

Once the file system has been set up, the file can be read using the `fs.readFile()` method. This method takes two parameters: the file path, and a callback function. The callback function takes two parameters: an error object and the contents of the file.

```javascript
fs.readFile(filePath, (err, data) => {
  if (err) {
    console.error(err);
    return;
  }
  // Do something with the data
});
```

**Section 3: Splitting the File into Lines**

Once the file has been read, it needs to be split into individual lines. This can be done by using the `split()` method on the data. This method takes a string as a parameter, which will be used to split the data into individual lines.

```javascript
const lines = data.split('\n');
```

**Section 4: Iterating Over the Lines**

Finally, the lines can be iterated over using a `for` loop. This loop will loop over each line and log it to the console.

```javascript
for (let line of lines) {
  console.log(line);
}
```
