---
title: See if any elements of one array are present in another array in javascript
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-03 00:00:00
updated_at: 2023-02-03 00:00:00
tldr: The Array.prototype.some() method can be used to check if an array contains any element of another array.
---

**Contents**

[TOC]

**Section 1: Using the .some() Method**

The .some() method can be used to check if an array contains any element of another array. It takes a callback function as an argument and returns true if the callback function returns true for any element in the array.

**Section 2: Example Code**

Here is an example of using the .some() method to check if an array contains any element of another array:

```javascript
let arr1 = [1, 2, 3, 4];
let arr2 = [3, 4, 5, 6];

let result = arr1.some(el => arr2.includes(el));
console.log(result); // true
```

**Section 3: Using the .filter() Method**

The .filter() method can also be used to check if an array contains any element of another array. It takes a callback function as an argument and returns an array containing all elements that pass the test implemented by the callback function.

**Section 4: Example Code**

Here is an example of using the .filter() method to check if an array contains any element of another array:

```javascript
let arr1 = [1, 2, 3, 4];
let arr2 = [3, 4, 5, 6];

let result = arr1.filter(el => arr2.includes(el));
console.log(result); // [3, 4]
```
