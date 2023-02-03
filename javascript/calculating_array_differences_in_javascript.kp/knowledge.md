---
title: What is the most efficient way to find the difference between two arrays in javascript?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-03 00:00:00
updated_at: 2023-02-03 00:00:00
tldr: The difference between two arrays can be found using the Array.prototype.filter() method.
---

**Contents**

[TOC]

## Using forEach

Using the `forEach` method, we can loop through each element of both arrays and compare them. If the elements are not equal, we can add the element from the first array to a new array.

```javascript
const arr1 = [1, 2, 3, 4, 5];
const arr2 = [2, 4, 6];

let difference = [];

arr1.forEach((i) => {
  if (!arr2.includes(i)) {
    difference.push(i);
  }
});

console.log(difference); // [1, 3, 5]
```

## Using filter

Using the `filter` method, we can filter out elements from the first array that are not present in the second array.

```javascript
const arr1 = [1, 2, 3, 4, 5];
const arr2 = [2, 4, 6];

let difference = arr1.filter((x) => !arr2.includes(x));

console.log(difference); // [1, 3, 5]
```

## Using reduce

Using the `reduce` method, we can loop through each element of the first array and check if it is present in the second array. If it is not, we can add it to a new array.

```javascript
const arr1 = [1, 2, 3, 4, 5];
const arr2 = [2, 4, 6];

let difference = arr1.reduce((acc, curr) => {
  if (!arr2.includes(curr)) {
    acc.push(curr);
  }
  return acc;
}, []);

console.log(difference); // [1, 3, 5]
```

## Using Set

Using the `Set` object, we can create a set from the first array and then use the `difference` method to get the difference between the two sets.

```javascript
const arr1 = [1, 2, 3, 4, 5];
const arr2 = [2, 4, 6];

let set1 = new Set(arr1);
let set2 = new Set(arr2);

let difference = [...set1].filter((x) => !set2.has(x));

console.log(difference); // [1, 3, 5]
```
