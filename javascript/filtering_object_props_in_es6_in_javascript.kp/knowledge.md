---
title: Select object properties by key in es6
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-04 00:00:00
updated_at: 2023-02-04 00:00:00
tldr: Object.entries(obj) can be used to filter object properties by key in ES6.
---

**Contents**

[TOC]

# Section 1: Overview

In ES6, it is possible to filter object properties by key using the `Object.entries()` and `Array.prototype.filter()` methods. This approach allows us to create a new object with only the desired properties.

# Section 2: Object.entries()

The `Object.entries()` method takes an object as an argument and returns an array of key-value pairs. This array can then be used to filter the object's properties.

# Section 3: Array.prototype.filter()

The `Array.prototype.filter()` method takes a callback function as an argument, which is used to filter the array. This method returns a new array with only the elements that pass the test implemented by the callback function.

# Section 4: Example

For example, consider the following object:

```
const obj = {
  a: 1,
  b: 2,
  c: 3,
  d: 4
};
```

To filter this object by key, we can use the `Object.entries()` and `Array.prototype.filter()` methods:

```
const filteredObj = Object.entries(obj)
  .filter(([key]) => key === 'a' || key === 'c')
  .reduce((acc, [key, value]) => ({ ...acc, [key]: value }), {});

console.log(filteredObj); // { a: 1, c: 3 }
```
