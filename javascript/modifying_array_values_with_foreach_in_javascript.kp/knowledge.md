---
title: Alter elements in the array while looping through it with a foreach
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-04 00:00:00
updated_at: 2023-02-04 00:00:00
tldr: Yes, you can modify the values of the array elements when using a `forEach()` loop.
---

**Contents**

[TOC]

### Using the Array.prototype.map() Method
The `Array.prototype.map()` method can be used to modify the values of an array when doing a `forEach` loop. This method takes a callback function as an argument, which is then called for each element in the array. This callback function can be used to modify the value of each element in the array.

For example, if we want to increase the value of each element in an array by 2, we can use the `Array.prototype.map()` method as follows:

```javascript
let arr = [1, 2, 3, 4, 5];

let newArr = arr.map(function(elem) {
  return elem + 2;
});

console.log(newArr);
// Output: [3, 4, 5, 6, 7]
```

### Using the Array.prototype.forEach() Method
The `Array.prototype.forEach()` method can also be used to modify the values of an array when looping through it. This method takes a callback function as an argument, which is then called for each element in the array. This callback function can be used to modify the value of each element in the array.

For example, if we want to increase the value of each element in an array by 2, we can use the `Array.prototype.forEach()` method as follows:

```javascript
let arr = [1, 2, 3, 4, 5];

arr.forEach(function(elem, index) {
  arr[index] = elem + 2;
});

console.log(arr);
// Output: [3, 4, 5, 6, 7]
```

### Using the Array.prototype.reduce() Method
The `Array.prototype.reduce()` method can also be used to modify the values of an array when looping through it. This method takes a callback function as an argument, which is then called for each element in the array. This callback function can be used to modify the value of each element in the array.

For example, if we want to increase the value of each element in an array by 2, we can use the `Array.prototype.reduce()` method as follows:

```javascript
let arr = [1, 2, 3, 4, 5];

let newArr = arr.reduce(function(acc, elem) {
  acc.push(elem + 2);
  return acc;
}, []);

console.log(newArr);
// Output: [3, 4, 5, 6, 7]
```
