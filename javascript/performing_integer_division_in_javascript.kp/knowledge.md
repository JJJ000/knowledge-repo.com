---
title: What is the syntax for dividing two integers and obtaining the remainder in javascript?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-03 00:00:00
updated_at: 2023-02-03 00:00:00
tldr: To perform an integer division and get the remainder in JavaScript, use the modulo operator (%) to divide the two numbers and assign the remainder to a variable.
---

**Contents**

[TOC]

### Using the Division Operator

The division operator (`/`) can be used to perform an integer division in JavaScript. The result of the division will be a number that is rounded down to the nearest whole number.

For example, `10 / 3` will return `3`.

### Using the Math.floor() Method

The `Math.floor()` method can also be used to perform an integer division in JavaScript. This method will round the result of the division down to the nearest whole number.

For example, `Math.floor(10 / 3)` will return `3`.

### Getting the Remainder

The remainder of an integer division can be obtained using the modulo operator (`%`). The modulo operator returns the remainder of a division operation.

For example, `10 % 3` will return `1`.

### Combining the Methods

The division operator and the modulo operator can be combined to both perform an integer division and get the remainder in one operation.

For example, `Math.floor(10 / 3) % 3` will return `1`.
