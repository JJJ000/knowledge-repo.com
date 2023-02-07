---
title: Create a file and store it using javascript
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: A file can be created and saved using the FileSystem API in JavaScript.
---

**Contents**

[TOC]

## Creating a File

Using the File System module in Node.js, we can create a file with JavaScript. We can use the `fs.open()` method to create a file. This method takes two arguments: the path of the file to create and a flag that determines the file's behavior: 

```js
const fs = require('fs');

fs.open('myfile.txt', 'w', (err, file) => {
  if (err) throw err;
  console.log('File created successfully.');
});
```

## Writing to a File

Once the file is created, we can use the `fs.writeFile()` method to write data to the file. This method takes three arguments: the path of the file to write to, the data to write, and a callback function that is executed after the data is written. 

```js
const fs = require('fs');

fs.writeFile('myfile.txt', 'Hello World!', (err) => {
  if (err) throw err;
  console.log('Data written to file.');
});
```

## Saving a File

Once the data is written to the file, we can use the `fs.close()` method to save the file. This method takes two arguments: the file descriptor returned by `fs.open()` and a callback function that is executed after the file is closed. 

```js
const fs = require('fs');

fs.open('myfile.txt', 'w', (err, file) => {
  if (err) throw err;
  fs.writeFile('myfile.txt', 'Hello World!', (err) => {
    if (err) throw err;
    fs.close(file, (err) => {
      if (err) throw err;
      console.log('File saved successfully.');
    });
  });
});
```
