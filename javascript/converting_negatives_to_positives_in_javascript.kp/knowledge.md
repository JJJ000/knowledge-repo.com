---
title: Change the sign of a negative number to positive in javascript
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-04 00:00:00
updated_at: 2023-02-04 00:00:00
tldr: Use the Math.abs() method to convert a negative number to a positive one.
---

**Contents**

[TOC]

# Math.abs()

The `Math.abs()` method can be used to convert a negative number to a positive one in JavaScript. This method returns the absolute value of a number, which is the number without any negative sign.

Example:

```
let num = -5;
let absoluteValue = Math.abs(num);
console.log(absoluteValue); // Output: 5
```

# Multiply by -1

Another way to convert a negative number to a positive one in JavaScript is to multiply it by -1. This will change the sign of the number from negative to positive.

Example:

```
let num = -5;
let positiveNum = num * -1;
console.log(positiveNum); // Output: 5
```

# if/else Statement

Using an `if/else` statement, we can check if a number is negative or positive and then convert it accordingly. If the number is negative, we can multiply it by -1 to make it positive.

Example:

```
let num = -5;
let positiveNum;

if (num < 0) {
  positiveNum = num * -1;
} else {
  positiveNum = num;
}

console.log(positiveNum); // Output: 5
```
