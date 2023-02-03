---
title: Edit the length of a string in javascript
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-03 00:00:00
updated_at: 2023-02-03 00:00:00
tldr: Use the String.prototype.trim() method to trim a string in JavaScript.
---

**Contents**

[TOC]

1. Using `String.prototype.trim()` 

This method removes whitespace from both ends of a string.

```javascript
let str = "   Hello World!   ";

console.log(str.trim()); // Outputs: "Hello World!"
```

2. Using `String.prototype.replace()`

This method searches a string for a specified value, or a regular expression, and returns a new string where the specified values are replaced.

```javascript
let str = "   Hello World!   ";

console.log(str.replace(/^\s+|\s+$/g, '')); // Outputs: "Hello World!"
```

3. Using `String.prototype.slice()`

This method extracts a section of a string and returns a new string.

```javascript
let str = "   Hello World!   ";

console.log(str.slice(1, -1)); // Outputs: "Hello World!"
```

4. Using `String.prototype.split()`

This method splits a string into an array of substrings, and returns the new array.

```javascript
let str = "   Hello World!   ";

console.log(str.split(' ').filter(Boolean).join(' ')); // Outputs: "Hello World!"
```
