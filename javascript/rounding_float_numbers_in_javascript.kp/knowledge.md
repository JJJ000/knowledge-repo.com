---
title: What is the process for rounding float numbers in javascript?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: Use the Math.round() method to round float numbers in JavaScript.
---

**Contents**

[TOC]

1. Rounding with Math.round()
--------------------------------
The Math.round() function in JavaScript is used to round a number to its nearest integer.

Syntax:

Math.round(x)

Parameters:
x: A number.

Return Value:
The rounded value of the given number.

Example:

```
var x = 5.5;
var y = Math.round(x);
console.log(y); // Output: 6
```

2. Rounding with toFixed()
------------------------------
The toFixed() method in JavaScript is used to format a number by adding zeroes to the end of the given number up to the number of decimal places specified.

Syntax:

number.toFixed(numOfDecimals)

Parameters:
numOfDecimals: The number of decimal places to which the number should be rounded.

Return Value:
A string representing the given number rounded to the specified number of decimal places.

Example:

```
var x = 5.56789;
var y = x.toFixed(2);
console.log(y); // Output: 5.57
```

3. Rounding with Math.ceil()
-----------------------------
The Math.ceil() function in JavaScript is used to round a number to its nearest upper integer.

Syntax:

Math.ceil(x)

Parameters:
x: A number.

Return Value:
The rounded value of the given number.

Example:

```
var x = 5.5;
var y = Math.ceil(x);
console.log(y); // Output: 6
```

4. Rounding with Math.floor()
------------------------------
The Math.floor() function in JavaScript is used to round a number to its nearest lower integer.

Syntax:

Math.floor(x)

Parameters:
x: A number.

Return Value:
The rounded value of the given number.

Example:

```
var x = 5.5;
var y = Math.floor(x);
console.log(y); // Output: 5
```
