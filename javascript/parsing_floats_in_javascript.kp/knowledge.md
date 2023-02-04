---
title: What is the syntax for rounding a float to two decimal places in javascript?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-04 00:00:00
updated_at: 2023-02-04 00:00:00
tldr: Use the `Number.parseFloat()` method with the second argument set to `2` to parse float with two decimal places in JavaScript.
---

**Contents**

[TOC]

### Using toFixed()

The `toFixed()` method can be used to parse a float with two decimal places. This method takes one argument, the number of decimal places to round to.

```js
var num = 2.56789;
var result = num.toFixed(2);
// result is 2.57
```

### Using Number()

The `Number()` method can also be used to parse a float with two decimal places. This method takes two arguments, the float and the number of decimal places to round to.

```js
var num = 2.56789;
var result = Number(num).toFixed(2);
// result is 2.57
```

### Using Math.round()

The `Math.round()` method can be used to round a float to the nearest integer. This method takes one argument, the float to round.

```js
var num = 2.56789;
var result = Math.round(num * 100) / 100;
// result is 2.57
```

### Using String.slice()

The `String.slice()` method can be used to parse a float with two decimal places. This method takes two arguments, the start index and the end index of the string.

```js
var num = 2.56789;
var result = num.toString().slice(0,4);
// result is 2.56
```
