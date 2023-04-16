---
title: How to combine two arrays in JavaScript and remove duplicate elements
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Use the spread operator (...) and the Set object to merge two arrays and de-duplicate items in JavaScript.
---

**Contents**

[TOC]

### 1. Combining Arrays

JavaScript provides several methods for combining two or more arrays. The simplest and most commonly used is the `concat()` method. This method takes one or more arrays as arguments and returns a new array containing all the elements of the original arrays.

```javascript
var arr1 = [1, 2, 3];
var arr2 = [4, 5, 6];

var combinedArr = arr1.concat(arr2);
// combinedArr = [1, 2, 3, 4, 5, 6]
```

### 2. De-duplicating Items

Once the two arrays have been combined, the next step is to remove any duplicate items. JavaScript provides a `Set()` object which provides a means of removing duplicate items from an array.

```javascript
var arr = [1, 2, 3, 4, 5, 6, 1, 2, 3];

var uniqueArr = Array.from(new Set(arr));
// uniqueArr = [1, 2, 3, 4, 5, 6]
```

### 3. Combining and De-duplicating

The `concat()` and `Set()` methods can be used together to combine two arrays and remove any duplicate items.

```javascript
var arr1 = [1, 2, 3];
var arr2 = [4, 5, 6, 1, 2, 3];

var combinedArr = Array.from(new Set(arr1.concat(arr2)));
// combinedArr = [1, 2, 3, 4, 5, 6]
```

### 4. ES6 Spread Operator

The ES6 spread operator (`...`) can also be used to combine two arrays and remove any duplicate items.

```javascript
var arr1 = [1, 2, 3];
var arr2 = [4, 5, 6, 1, 2, 3];

var combinedArr = [...new Set([...arr1, ...arr2])];
// combinedArr = [1, 2, 3, 4, 5, 6]
```
