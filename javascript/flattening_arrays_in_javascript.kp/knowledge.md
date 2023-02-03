---
title: Combine the elements of multiple arrays into one array
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-03 00:00:00
updated_at: 2023-02-03 00:00:00
tldr: Use the Array.prototype.flat() method to flatten an array of arrays in Javascript.
---

**Contents**

[TOC]

**Section 1: Overview**
Merging/flattening an array of arrays in JavaScript is a simple task that can be accomplished using a variety of methods. The most common methods involve looping through the array and either pushing the elements into a new array or using the spread operator.

**Section 2: Using a Loop**
The simplest way to merge/flatten an array of arrays is to use a loop. This can be done by looping through the array, then looping through each element and pushing each element into a new array. For example:

```javascript
const array = [[1,2,3], [4,5,6], [7,8,9]];
const newArray = [];

for (let i = 0; i < array.length; i++) {
  for (let j = 0; j < array[i].length; j++) {
    newArray.push(array[i][j]);
  }
}

console.log(newArray); // [1, 2, 3, 4, 5, 6, 7, 8, 9]
```

**Section 3: Using the Spread Operator**
Another way to merge/flatten an array of arrays is to use the spread operator. This can be done by looping through the array and using the spread operator to add each element to a new array. For example:

```javascript
const array = [[1,2,3], [4,5,6], [7,8,9]];
const newArray = [];

for (let i = 0; i < array.length; i++) {
  newArray.push(...array[i]);
}

console.log(newArray); // [1, 2, 3, 4, 5, 6, 7, 8, 9]
```

**Section 4: Using Array.prototype.concat()**
The Array.prototype.concat() method can also be used to merge/flatten an array of arrays. This can be done by looping through the array and using the concat() method to add each element to a new array. For example:

```javascript
const array = [[1,2,3], [4,5,6], [7,8,9]];
const newArray = [];

for (let i = 0; i < array.length; i++) {
  newArray = newArray.concat(array[i]);
}

console.log(newArray); // [1, 2, 3, 4, 5, 6, 7, 8, 9]
```
