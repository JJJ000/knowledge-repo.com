---
title: What is the best way to turn a float number into an integer in javascript?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-03 00:00:00
updated_at: 2023-02-03 00:00:00
tldr: Use the Math.round() function to round a float number to the nearest whole number.
---

**Contents**

[TOC]

### Using Math.trunc()

The Math.trunc() method is used to remove the fractional part of a number and return the integer part.

Syntax:
```
Math.trunc(number)
```

Example:
```
Math.trunc(3.14); // 3
```

### Using Math.floor()

The Math.floor() method is used to round a number down to the nearest integer.

Syntax:
```
Math.floor(number)
```

Example:
```
Math.floor(3.14); // 3
```

### Using Math.ceil()

The Math.ceil() method is used to round a number up to the nearest integer.

Syntax:
```
Math.ceil(number)
```

Example:
```
Math.ceil(3.14); // 4
```

### Using parseInt()

The parseInt() method is used to convert a string to an integer.

Syntax:
```
parseInt(string, radix)
```

Example:
```
parseInt("3.14", 10); // 3
```
