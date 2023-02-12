---
title: Combine two json/javascript arrays into a single array
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-12 00:00:00
updated_at: 2023-02-12 00:00:00
tldr: Use the spread operator (...) to combine the two arrays into one.
---

**Contents**

[TOC]

### Section 1: Concatenation

The simplest way to merge two JavaScript arrays is to use the `concat()` method. This method does not modify the original arrays, but instead returns a new array with the elements of both arrays combined.

```
let array1 = [1, 2, 3];
let array2 = [4, 5, 6];

let combinedArray = array1.concat(array2);

console.log(combinedArray); // [1, 2, 3, 4, 5, 6]
```

### Section 2: Spread Syntax

Another way to merge two JavaScript arrays is to use the spread syntax. This method also does not modify the original arrays, but instead returns a new array with the elements of both arrays combined.

```
let array1 = [1, 2, 3];
let array2 = [4, 5, 6];

let combinedArray = [...array1, ...array2];

console.log(combinedArray); // [1, 2, 3, 4, 5, 6]
```

### Section 3: Array.prototype.push()

The `Array.prototype.push()` method can also be used to merge two JavaScript arrays. Unlike the previous two methods, this method modifies the original array by adding the elements of the second array to the end of the first array.

```
let array1 = [1, 2, 3];
let array2 = [4, 5, 6];

array1.push(...array2);

console.log(array1); // [1, 2, 3, 4, 5, 6]
```

### Section 4: Array.prototype.unshift()

The `Array.prototype.unshift()` method is similar to the `Array.prototype.push()` method, but instead of adding the elements of the second array to the end of the first array, it adds them to the beginning of the first array.

```
let array1 = [1, 2, 3];
let array2 = [4, 5, 6];

array1.unshift(...array2);

console.log(array1); // [4, 5, 6, 1, 2, 3]
```
