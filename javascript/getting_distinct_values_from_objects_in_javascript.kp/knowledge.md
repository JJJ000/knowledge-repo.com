---
title: What is the most efficient way to extract unique values from an array of objects in javascript?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-03 00:00:00
updated_at: 2023-02-03 00:00:00
tldr: Use the Array.prototype.filter() method to filter out duplicate elements from the array of objects.
---

**Contents**

[TOC]

### 1. Using a Set
A Set is a collection of unique values. We can use the Set object to store the array elements and then get the distinct values.

```javascript
// Create an array of objects
let arr = [
  {name: 'John', age: 20},
  {name: 'John', age: 22},
  {name: 'Jane', age: 20},
  {name: 'Tom', age: 22}
];

// Create a Set
let set = new Set();

// Loop through the array
arr.forEach(item => {
  // Add the object to the Set
  set.add(JSON.stringify(item));
});

// Get the distinct values
let distinctValues = Array.from(set).map(item => JSON.parse(item));

console.log(distinctValues);
// [
//   {name: 'John', age: 20},
//   {name: 'John', age: 22},
//   {name: 'Jane', age: 20},
//   {name: 'Tom', age: 22}
// ]
```

### 2. Using a Map
A Map is an object that stores a key-value pair. We can use the Map object to store the array elements and then get the distinct values.

```javascript
// Create an array of objects
let arr = [
  {name: 'John', age: 20},
  {name: 'John', age: 22},
  {name: 'Jane', age: 20},
  {name: 'Tom', age: 22}
];

// Create a Map
let map = new Map();

// Loop through the array
arr.forEach(item => {
  // Add the object to the Map
  map.set(JSON.stringify(item), item);
});

// Get the distinct values
let distinctValues = Array.from(map.values());

console.log(distinctValues);
// [
//   {name: 'John', age: 20},
//   {name: 'John', age: 22},
//   {name: 'Jane', age: 20},
//   {name: 'Tom', age: 22}
// ]
```

### 3. Using Array.filter()
We can use the Array.filter() method to filter out the duplicate objects from the array.

```javascript
// Create an array of objects
let arr = [
  {name: 'John', age: 20},
  {name: 'John', age: 22},
  {name: 'Jane', age: 20},
  {name: 'Tom', age: 22}
];

// Create an empty array
let distinctValues = [];

// Loop through the array
arr.forEach(item => {
  // Check if the object is already in the array
  let isDuplicate = distinctValues.some(distinctItem => {
    return JSON.stringify(distinctItem) === JSON.stringify(item);
  });

  // If not, add it to the array
  if (!isDuplicate) {
    distinctValues.push(item);
  }
});

console.log(distinctValues);
// [
//   {name: 'John', age: 20},
//   {name: 'John', age: 22},
//   {name: 'Jane', age: 20},
//   {name: 'Tom', age: 22}
// ]
```

### 4. Using Array.reduce()
We can use the Array.reduce() method to reduce the array to a single object and get the distinct values.

```javascript
// Create an array of objects
let arr = [
  {name: 'John', age: 20},
  {name: 'John', age: 22},
  {name: 'Jane', age: 20},
  {name: 'Tom', age: 22}
];

// Reduce the array to a single object
let distinctValues = arr.reduce((acc, item) => {
  // Check if the object is already in the object
  let isDuplicate = Object.values(acc).some(distinctItem => {
    return JSON.stringify(distinctItem) === JSON.stringify(item);
  });

  // If not, add it to the object
  if (!isDuplicate) {
    acc[Object.keys(acc).length] = item;
  }

  return acc;
},
