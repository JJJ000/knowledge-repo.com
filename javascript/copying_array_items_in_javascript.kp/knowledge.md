---
title: Transfer elements from one array to another
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-03 00:00:00
updated_at: 2023-02-03 00:00:00
tldr: Use the Array.prototype.slice() or Array.prototype.concat() methods to copy items from one array into another.
---

**Contents**

[TOC]

### Using the Spread Operator

The spread operator (`...`) can be used to copy items from one array into another. 

```javascript
let arr1 = [1, 2, 3];
let arr2 = [...arr1]; // arr2 is now [1, 2, 3]
```

### Using Array.prototype.slice()

The `Array.prototype.slice()` method can be used to copy items from one array into another.

```javascript
let arr1 = [1, 2, 3];
let arr2 = arr1.slice(); // arr2 is now [1, 2, 3]
```

### Using Array.from()

The `Array.from()` method can be used to copy items from one array into another.

```javascript
let arr1 = [1, 2, 3];
let arr2 = Array.from(arr1); // arr2 is now [1, 2, 3]
```

### Using the for loop

A `for` loop can be used to copy items from one array into another.

```javascript
let arr1 = [1, 2, 3];
let arr2 = [];

for (let i = 0; i < arr1.length; i++) {
  arr2.push(arr1[i]);
}

// arr2 is now [1, 2, 3]
```
