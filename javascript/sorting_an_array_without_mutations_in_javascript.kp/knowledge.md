---
title: What is the most efficient way to sort an array without altering the original array?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: You can use the Array.prototype.slice() method to create a shallow copy of the array, then use the Array.prototype.sort() method to sort the copy without mutating the original array.
---

**Contents**

[TOC]

### Using the Spread Operator

The spread operator (`...`) can be used to spread the elements of an array into a list of arguments for the `sort()` method. This will create a new sorted array without mutating the original array.

```js
const arr = [3, 2, 1];
const sorted = [...arr].sort();

console.log(arr); // [3, 2, 1]
console.log(sorted); // [1, 2, 3]
```

### Using the Array.prototype.slice() Method

The `slice()` method can be used to create a shallow copy of the array and the `sort()` method can be used to sort the shallow copy.

```js
const arr = [3, 2, 1];
const sorted = arr.slice().sort();

console.log(arr); // [3, 2, 1]
console.log(sorted); // [1, 2, 3]
```

### Using the Array.prototype.concat() Method

The `concat()` method can be used to concatenate the array with an empty array and the `sort()` method can be used to sort the new array.

```js
const arr = [3, 2, 1];
const sorted = arr.concat([]).sort();

console.log(arr); // [3, 2, 1]
console.log(sorted); // [1, 2, 3]
```

### Using the Array.prototype.map() Method

The `map()` method can be used to create a new array by mapping each element of the original array to itself. The `sort()` method can then be used to sort the new array.

```js
const arr = [3, 2, 1];
const sorted = arr.map(x => x).sort();

console.log(arr); // [3, 2, 1]
console.log(sorted); // [1, 2, 3]
```
