---
title: Find the decimal portion of a number using javascript
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: To get the decimal portion of a number with JavaScript, use the modulo operator (%) to get the remainder of the division of the number by 1.
---

**Contents**

[TOC]

### Using the Modulus Operator

The modulus operator can be used to get the decimal portion of a number. The modulus operator returns the remainder of a division operation.

Syntax:
```
x % y
```

Example:
```
var num = 15.67;
var decimal = num % 1;
// decimal = 0.67
```

### Using the toFixed() Method

The toFixed() method can be used to get the decimal portion of a number. The toFixed() method rounds a number to a specified number of digits after the decimal point.

Syntax:
```
number.toFixed(digits);
```

Example:
```
var num = 15.67;
var decimal = num.toFixed(2).substring(2);
// decimal = 0.67
```
