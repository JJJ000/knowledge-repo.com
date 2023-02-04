---
title: Add leading zeros to a number in javascript
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-04 00:00:00
updated_at: 2023-02-04 00:00:00
tldr: Use the toString() method with a specified radix to pad a number with leading zeros.
---

**Contents**

[TOC]

**Solution 1: Using padStart()**

The padStart() method can be used to pad a number with leading zeros. It takes two parameters: the length of the resulting string and the character to pad with.

```
let num = 5;
let paddedNum = num.toString().padStart(4, '0');

console.log(paddedNum); // Outputs "0005"
```

**Solution 2: Using String.prototype.repeat()**

The String.prototype.repeat() method can also be used to pad a number with leading zeros. It takes one parameter: the number of times to repeat the character.

```
let num = 5;
let paddedNum = '0'.repeat(4 - num.toString().length) + num;

console.log(paddedNum); // Outputs "0005"
```
