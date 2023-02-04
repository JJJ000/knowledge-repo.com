---
title: Change all the spaces in a string to '+'
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-04 00:00:00
updated_at: 2023-02-04 00:00:00
tldr: String.prototype.replace(/\s/g, `+`);
---

**Contents**

[TOC]

**Solution 1**

Using `replace()` Method:

```javascript
let str = "Replace all spaces";
let newStr = str.replace(/\s/g, "+");
console.log(newStr); // Output: Replace+all+spaces
```

**Solution 2**

Using `split()` and `join()` Methods:

```javascript
let str = "Replace all spaces";
let newStr = str.split(' ').join('+');
console.log(newStr); // Output: Replace+all+spaces
```
