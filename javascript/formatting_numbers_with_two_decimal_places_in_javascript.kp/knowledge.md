---
title: Display number with two decimal places
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-03 00:00:00
updated_at: 2023-02-03 00:00:00
tldr: Use the toFixed() method to format a number to always show two decimal places.
---

**Contents**

[TOC]

**Solution 1**

Using `toFixed()` Method:

```javascript
let num = 10.5;
let result = num.toFixed(2);
console.log(result); // 10.50
```

**Solution 2**

Using `Number.prototype.toFixed()` Method:

```javascript
let num = 10.5;
let result = Number(num).toFixed(2);
console.log(result); // 10.50
```
