---
title: A JavaScript function that shares similarities with python's range() function
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-16 00:00:00
updated_at: 2023-04-16 00:00:00
tldr: The JavaScript function similar to Python range() is the Array.from() method.
---

**Contents**

[TOC]

## Introduction

Python has a built-in function called range() which generates a sequence of integers. It is often used in for loops to iterate over a range of numbers. JavaScript doesn't have a built-in equivalent to the range() function, but it can be easily implemented with a custom function.

## Implementing a JavaScript Range Function

Here's an implementation of a JavaScript range() function that takes three arguments - start, stop, and step - and returns an array of numbers representing the range:

```javascript
function range(start, stop, step) {
  if (typeof stop == 'undefined') {
    // if only one argument is passed
    stop = start;
    start = 0;
  }
  if (typeof step == 'undefined') {
    step = 1;
  }
  if ((step > 0 && start >= stop) || (step < 0 && start <= stop)) {
    return [];
  }
  var res = [];
  for (var i = start; step > 0 ? i < stop : i > stop; i += step) {
    res.push(i);
  }
  return res;
}
```

## Using the JavaScript Range Function

The range() function can be used to generate a sequence of numbers just like the Python range() function. Here are some examples:

```javascript
var r1 = range(5);
console.log(r1); // [0, 1, 2, 3, 4]

var r2 = range(1, 5);
console.log(r2); // [1, 2, 3, 4]

var r3 = range(0, 10, 2);
console.log(r3); // [0, 2, 4, 6, 8]

var r4 = range(10, 0, -1);
console.log(r4); // [10, 9, 8, 7, 6, 5, 4, 3, 2, 1]
```

## Conclusion

Although JavaScript doesn't have a built-in equivalent to Python's range() function, it can be easily implemented with a custom function. The range() function can take three arguments - start, stop, and step - and returns an array of numbers representing the range. It can be used in for loops to iterate over a range of numbers just like the Python range() function.
