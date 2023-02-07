---
title: How to calculate the total of a property in an array
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: Use the Array.prototype.reduce() method to sum the values of a property in an array.
---

**Contents**

[TOC]

### 1. Using `forEach()`

The `forEach()` method is an easy way to sum the values of a property in an array. It takes a callback function as an argument, which is invoked for each element in the array. Within the callback function, we can access the value of the property and add it to a total sum.

```javascript
let totalSum = 0;

arr.forEach(function(item) {
  totalSum += item.property;
});
```

### 2. Using `reduce()`

The `reduce()` method is another way to sum the values of a property in an array. It takes a callback function as an argument, which is invoked for each element in the array. Within the callback function, we can access the value of the property and add it to an accumulator.

```javascript
let totalSum = arr.reduce(function(acc, item) {
  return acc + item.property;
}, 0);
```

### 3. Using `for...of`

The `for...of` loop is another way to sum the values of a property in an array. It iterates over each element in the array, and within the loop, we can access the value of the property and add it to a total sum.

```javascript
let totalSum = 0;

for (let item of arr) {
  totalSum += item.property;
}
```

### 4. Using `Array.prototype.map()`

The `Array.prototype.map()` method is yet another way to sum the values of a property in an array. It takes a callback function as an argument, which is invoked for each element in the array. Within the callback function, we can access the value of the property and return it as an array of values. We can then use the `Array.prototype.reduce()` method to sum the values of the array.

```javascript
let totalSum = arr.map(function(item) {
  return item.property;
}).reduce(function(acc, value) {
  return acc + value;
}, 0);
```
