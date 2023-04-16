---
title: What is the method for determining if a number is nan in javascript?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: You can check if a number is NaN in JavaScript by using the isNaN() function.
---

**Contents**

[TOC]

### Using the isNaN() Function
The `isNaN()` function is the most reliable way to check if a value is a number or not. This function returns `true` if the value is `NaN` and `false` if it is a number.

### Example

```
let x = NaN;

console.log(isNaN(x)); // Output: true
```

### Using the typeof Operator
The `typeof` operator can also be used to check if a value is `NaN`. The `typeof` operator will return `"number"` if the value is a number and `"NaN"` if the value is `NaN`.

### Example

```
let x = NaN;

console.log(typeof x); // Output: NaN
```
