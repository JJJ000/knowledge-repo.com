---
title: The quickest method to add a value to the beginning of an array
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: The most efficient way to prepend a value to an array in Javascript is to use the unshift() method.
---

**Contents**

[TOC]

**Using Array.prototype.unshift()**

1. Definition:
   Array.prototype.unshift() is a method that adds one or more elements to the beginning of an array and returns the new length of the array. 

2. Syntax:
   array.unshift(element1[, ...[, elementN]])

3. Example:
   ```javascript
   let array = [1, 2, 3];
   array.unshift(4);
   console.log(array); // [4, 1, 2, 3]
   ```

**Using Array Spread Syntax**

1. Definition:
   Array spread syntax allows an expression to be expanded in places where multiple arguments (for function calls) or multiple elements (for array literals) are expected.

2. Syntax:
   [element1, ...array]

3. Example:
   ```javascript
   let array = [1, 2, 3];
   let newArray = [4, ...array];
   console.log(newArray); // [4, 1, 2, 3]
   ```
