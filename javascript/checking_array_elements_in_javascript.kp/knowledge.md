---
title: See if an item is included in an array
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: You can use the Array.includes() method to check if an element is present in an array.
---

**Contents**

[TOC]

### Using `Array.prototype.includes()`

The `Array.prototype.includes()` method can be used to check if an element is present in an array. This method returns `true` if the element is present in the array, and `false` if it is not.

Example:

```js
const arr = [1, 2, 3];

arr.includes(2); // returns true
arr.includes(4); // returns false
```

### Using `Array.prototype.indexOf()`

The `Array.prototype.indexOf()` method can also be used to check if an element is present in an array. This method returns the index of the element if it is present in the array, and `-1` if it is not.

Example:

```js
const arr = [1, 2, 3];

arr.indexOf(2); // returns 1
arr.indexOf(4); // returns -1
```

### Using `Array.prototype.some()`

The `Array.prototype.some()` method can be used to check if an element is present in an array. This method returns `true` if at least one element in the array satisfies the provided testing function, and `false` if none of the elements satisfy the testing function.

Example:

```js
const arr = [1, 2, 3];

arr.some(el => el === 2); // returns true
arr.some(el => el === 4); // returns false
```

### Using `Array.prototype.find()`

The `Array.prototype.find()` method can be used to check if an element is present in an array. This method returns the value of the first element in the array that satisfies the provided testing function, and `undefined` if none of the elements satisfy the testing function.

Example:

```js
const arr = [1, 2, 3];

arr.find(el => el === 2); // returns 2
arr.find(el => el === 4); // returns undefined
```
