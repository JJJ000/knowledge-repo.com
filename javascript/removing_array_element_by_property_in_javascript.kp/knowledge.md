---
title: Delete array item based on object attribute
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: Use the Array.prototype.filter() method to create a new array based on a given condition that filters out the element with the specified object property.
---

**Contents**

[TOC]

### Using .filter()

The .filter() method can be used to create a new array with all elements that pass the test implemented by the provided function. This can be used to create a new array that does not contain the object with the specified property.

```javascript
let array = [
    { name: 'John', age: 30 },
    { name: 'Jane', age: 25 },
    { name: 'Tom', age: 28 }
];

let filteredArray = array.filter((item) => item.name !== 'Tom');

// filteredArray = [
//     { name: 'John', age: 30 },
//     { name: 'Jane', age: 25 }
// ]
```

### Using .splice()

The .splice() method can be used to remove elements from an array. This can be used to remove the object with the specified property.

```javascript
let array = [
    { name: 'John', age: 30 },
    { name: 'Jane', age: 25 },
    { name: 'Tom', age: 28 }
];

let index = array.findIndex((item) => item.name === 'Tom');
array.splice(index, 1);

// array = [
//     { name: 'John', age: 30 },
//     { name: 'Jane', age: 25 }
// ]
```
