---
title: Use the .join method on the values within an array of objects
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: The .join() method can be used to join the values in an array of objects into a string.
---

**Contents**

[TOC]

#### Using Array.prototype.reduce()

We can use the `Array.prototype.reduce()` method to join the values of an array of objects. The `reduce()` method applies a function against an accumulator and each element in the array (from left to right) to reduce it to a single value.

```js
let arrayOfObjects = [
  {
    key1: "value1",
    key2: "value2"
  },
  {
    key1: "value3",
    key2: "value4"
  }
];

let joinedValues = arrayOfObjects.reduce((acc, curr) => {
  return acc + curr.key1 + curr.key2;
}, "");

// joinedValues = "value1value2value3value4"
```

#### Using Array.prototype.map()

We can also use the `Array.prototype.map()` method to join the values of an array of objects. The `map()` method creates a new array populated with the results of calling a provided function on every element in the calling array.

```js
let arrayOfObjects = [
  {
    key1: "value1",
    key2: "value2"
  },
  {
    key1: "value3",
    key2: "value4"
  }
];

let joinedValues = arrayOfObjects.map(obj => obj.key1 + obj.key2).join("");

// joinedValues = "value1value2value3value4"
```
