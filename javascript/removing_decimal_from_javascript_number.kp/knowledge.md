---
title: What is the best way to truncate a JavaScript number to remove the decimal portion?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-08 00:00:00
updated_at: 2023-02-08 00:00:00
tldr: Use the Math.trunc() method to remove the decimal part from a JavaScript number.
---

**Contents**

[TOC]

**Option 1: Math.floor()**

Math.floor() is a built-in JavaScript method that can be used to remove the decimal part of a number. It rounds the number down to the nearest integer, effectively removing the decimal part.

Syntax:

```
Math.floor(number)
```

Example:

```
var num = 5.9;
var result = Math.floor(num);

// result = 5
```

**Option 2: toFixed()**

The toFixed() method is another built-in JavaScript method that can be used to remove the decimal part of a number. It returns a string representation of the number with the specified number of decimal places.

Syntax:

```
number.toFixed(numberOfDecimals)
```

Example:

```
var num = 5.9;
var result = num.toFixed(0);

// result = "5"
```

**Option 3: parseInt()**

The parseInt() method is another built-in JavaScript method that can be used to remove the decimal part of a number. It parses a string argument and returns an integer of the specified radix or base.

Syntax:

```
parseInt(string, radix)
```

Example:

```
var num = 5.9;
var result = parseInt(num, 10);

// result = 5
```

**Option 4: Math.trunc()**

Math.trunc() is a newer built-in JavaScript method that can be used to remove the decimal part of a number. It returns the integer part of a number by removing any fractional digits.

Syntax:

```
Math.trunc(number)
```

Example:

```
var num = 5.9;
var result = Math.trunc(num);

// result = 5
```
