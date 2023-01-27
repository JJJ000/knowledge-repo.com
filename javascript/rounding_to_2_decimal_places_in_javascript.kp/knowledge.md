---
title: What is the process for rounding a number to a maximum of two decimal places, if needed?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-01-27 00:00:00
updated_at: 2023-01-27 00:00:00
tldr: Use the .toFixed(2) method to round a number to at most 2 decimal places if necessary in Javascript.
---

**Contents**

[TOC]

### Using Math.round()

The Math.round() function can be used to round a number to the nearest integer. By multiplying the number by 100, the number can be rounded to the nearest hundredth, and then divided by 100 to return the number to its original form.

```javascript
let num = 3.14159;
let rounded = Math.round(num * 100) / 100;
console.log(rounded); // 3.14
```

### Using toFixed()

The toFixed() method can also be used to round a number to the nearest decimal place. The number of decimal places is determined by the number passed into the toFixed() method.

```javascript
let num = 3.14159;
let rounded = num.toFixed(2);
console.log(rounded); // 3.14
```

### Using Number.prototype.toFixed()

The Number.prototype.toFixed() method can also be used to round a number to the nearest decimal place. The number of decimal places is determined by the number passed into the toFixed() method. 

```javascript
let num = 3.14159;
let rounded = Number.prototype.toFixed.call(num, 2);
console.log(rounded); // 3.14
```
