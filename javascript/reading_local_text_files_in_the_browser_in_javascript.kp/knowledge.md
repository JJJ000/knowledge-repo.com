---
title: What is the process for accessing a text file stored on the local computer through a web browser?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-04 00:00:00
updated_at: 2023-02-04 00:00:00
tldr: Use the FileReader API to read a local text file in the browser in Javascript.
---

**Contents**

[TOC]

# Section 1 - Create a FileReader Object

The first step is to create a `FileReader` object. This object is used for reading the contents of a file. The `FileReader` object can be created with the following code:

```javascript
var reader = new FileReader();
```

# Section 2 - Assign a File to the FileReader

The next step is to assign a file to the `FileReader` object. This can be done using the `readAsText()` method, which takes a file object as its parameter. The file object can be obtained from an HTML `<input>` element.

```javascript
var input = document.getElementById('input');
reader.readAsText(input.files[0]);
```

# Section 3 - Read the File

Once the file is assigned to the `FileReader` object, the file can be read using the `readAsText()` method. This method returns a `Promise` object, which can be used to determine when the file has been read.

```javascript
reader.readAsText(input.files[0])
  .then(function(result) {
    // File has been read
  });
```

# Section 4 - Access the File Contents

Once the file has been read, the contents can be accessed using the `result` property of the `FileReader` object. This property contains the contents of the file as a string.

```javascript
reader.readAsText(input.files[0])
  .then(function(result) {
    // Access the contents of the file
    var contents = reader.result;
  });
```
