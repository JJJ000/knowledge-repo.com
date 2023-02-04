---
title: What is the syntax for formatting a float in javascript?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-04 00:00:00
updated_at: 2023-02-04 00:00:00
tldr: To format a float in JavaScript, use the toFixed() method.
---

**Contents**

[TOC]

### Using toFixed()

The `toFixed()` method is used to format a number to a specified number of decimal places. It takes one argument, which is the number of decimal places to round the number to.

Syntax:

```
num.toFixed(x)
```

Where `num` is the number to be formatted and `x` is the number of decimal places to round the number to.

### Example

To format a float to two decimal places, the syntax would be:

```
var num = 5.56789;
var n = num.toFixed(2);
```

The variable `n` would now contain the value `5.57`.
