---
title: What is the best way to remove a file extension from a string in javascript?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Use the String.prototype.replace() method to replace the file extension with an empty string.
---

**Contents**

[TOC]

## Using Substring

The `substring()` method can be used to trim a file extension from a string in JavaScript. This method takes two parameters, start and end index, and returns the part of the string between the start and end index, not including the end index itself.

For example, to trim the file extension `.jpg` from the string `image.jpg`, we can use the following code:

```js
var fileName = "image.jpg";
var trimmedFileName = fileName.substring(0, fileName.lastIndexOf("."));
// trimmedFileName = "image"
```

## Using Regular Expressions

Regular expressions can also be used to trim a file extension from a string in JavaScript. The `replace()` method can be used to replace a substring with a given string.

For example, to trim the file extension `.jpg` from the string `image.jpg`, we can use the following code:

```js
var fileName = "image.jpg";
var trimmedFileName = fileName.replace(/\.[^/.]+$/, "");
// trimmedFileName = "image"
```

## Using Split

The `split()` method can also be used to trim a file extension from a string in JavaScript. This method takes a separator as a parameter and splits the string into an array of substrings.

For example, to trim the file extension `.jpg` from the string `image.jpg`, we can use the following code:

```js
var fileName = "image.jpg";
var trimmedFileName = fileName.split(".")[0];
// trimmedFileName = "image"
```
