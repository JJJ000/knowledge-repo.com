---
title: What is the best way to shuffle an array in javascript?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: To randomize an array in JavaScript, use the Array.prototype.sort() method with a function that returns a random number.
---

**Contents**

[TOC]

### Using the sort() Method

The sort() method can be used to randomize an array by using a custom compare function. The compare function should return a random value (either a negative, positive, or zero). This random value will be used to sort the array.

Example:

```javascript
let arr = [1, 2, 3, 4, 5];

arr.sort(() => Math.random() - 0.5);
console.log(arr); // [4, 2, 5, 1, 3]
```

### Using the for Loop

The for loop can also be used to randomize an array. The for loop will iterate through the array and randomly swap two elements.

Example:

```javascript
let arr = [1, 2, 3, 4, 5];

for (let i = arr.length - 1; i > 0; i--) {
    let j = Math.floor(Math.random() * (i + 1));
    let temp = arr[i];
    arr[i] = arr[j];
    arr[j] = temp;
}
console.log(arr); // [2, 5, 3, 4, 1]
```

### Using the Fisher-Yates Algorithm

The Fisher-Yates algorithm is a popular algorithm for randomizing an array. This algorithm works by iterating through the array and randomly swapping two elements.

Example:

```javascript
let arr = [1, 2, 3, 4, 5];

for (let i = arr.length - 1; i > 0; i--) {
    let j = Math.floor(Math.random() * (i + 1));
    [arr[i], arr[j]] = [arr[j], arr[i]];
}
console.log(arr); // [3, 1, 5, 4, 2]
```

### Using the Lodash Library

The Lodash library provides a convenient way to randomize an array. The _.shuffle() method can be used to randomize an array.

Example:

```javascript
let arr = [1, 2, 3, 4, 5];

let shuffled = _.shuffle(arr);
console.log(shuffled); // [4, 2, 1, 5, 3]
```
