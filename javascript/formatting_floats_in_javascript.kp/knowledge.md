---
title: Showing a float in JavaScript with two decimal places
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: You can use the toFixed() method to display a float to 2 decimal places in JavaScript.
---

**Contents**

[TOC]

**Using toFixed() Method:**

The `toFixed()` method is used to convert a number into a string, keeping a specified number of decimals.

Syntax:
```
number.toFixed(x)
```

Example:
```
var num = 5.56789;
var n = num.toFixed(2);
```

Output:
```
5.57
```

**Using String Concatenation:**

String concatenation can also be used to convert a float to 2 decimal places.

Example:
```
var num = 5.56789;
var n = Math.round(num * 100) / 100;
```

Output:
```
5.57
```
