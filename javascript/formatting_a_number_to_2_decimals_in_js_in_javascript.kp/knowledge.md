---
title: Displaying a number with two decimal places in javascript
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-04 00:00:00
updated_at: 2023-02-04 00:00:00
tldr: Use the toFixed() method to format a number with exactly two decimals.
---

**Contents**

[TOC]

### Using toFixed()

The `toFixed()` method of the `Number` object can be used to format a number with exactly two decimals. This method takes one argument, which is the number of decimal places to include.

```javascript
var num = 5.56789;
var n = num.toFixed(2);
console.log(n); // Outputs "5.57"
```

### Using toPrecision()

The `toPrecision()` method of the `Number` object can also be used to format a number with exactly two decimals. This method takes one argument, which is the total number of digits to include.

```javascript
var num = 5.56789;
var n = num.toPrecision(4);
console.log(n); // Outputs "5.568"
```

### Using String.prototype.padStart()

The `String.prototype.padStart()` method can be used to format a number with exactly two decimals. This method takes two arguments, the first being the total length of the string to return, and the second being the character to use for padding.

```javascript
var num = 5.56789;
var n = num.toString().padStart(5, '0');
console.log(n); // Outputs "05.57"
```

### Using String.prototype.slice()

The `String.prototype.slice()` method can also be used to format a number with exactly two decimals. This method takes two arguments, the first being the starting index of the substring to return, and the second being the ending index of the substring to return.

```javascript
var num = 5.56789;
var n = num.toString().slice(0, 5);
console.log(n); // Outputs "5.56"
```
