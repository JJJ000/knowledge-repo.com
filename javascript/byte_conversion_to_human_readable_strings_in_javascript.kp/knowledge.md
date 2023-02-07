---
title: Changing the file size from bytes to a more easily understood format
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: The file size in bytes can be converted to a human-readable string by using the toLocaleString() method.
---

**Contents**

[TOC]

## Section 1: Introduction

Converting file size in bytes to a human-readable string is a common task in programming. It is useful for displaying the size of a file to a user in a more understandable format. In Javascript, this can be accomplished by using a few simple functions to convert the bytes into a more readable format.

## Section 2: Conversion Function

The following function can be used to convert a file size in bytes to a human-readable string:

```javascript
function bytesToSize(bytes) {
   var sizes = ['Bytes', 'KB', 'MB', 'GB', 'TB'];
   if (bytes == 0) return '0 Byte';
   var i = parseInt(Math.floor(Math.log(bytes) / Math.log(1024)));
   return Math.round(bytes / Math.pow(1024, i), 2) + ' ' + sizes[i];
}
```

This function takes the size of a file in bytes and converts it to a human-readable string. It uses an array of sizes (Bytes, KB, MB, GB, TB) to determine the appropriate size to display. It then uses the `Math.log()` and `Math.pow()` functions to calculate the correct size and returns the result as a string.

## Section 3: Usage

The function can be used as follows:

```javascript
var fileSize = 1024; // 1KB
var sizeString = bytesToSize(fileSize); // "1 KB"
```

## Section 4: Conclusion

In conclusion, converting file size in bytes to a human-readable string can be easily accomplished in Javascript using the `bytesToSize()` function. This function takes a size in bytes and returns a string with the size in a more understandable format. This can be useful for displaying file sizes to users in a more readable format.
