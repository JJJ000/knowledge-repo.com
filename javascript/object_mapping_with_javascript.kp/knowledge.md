---
title: Function to iterate through the properties of an object
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-02 00:00:00
updated_at: 2023-02-02 00:00:00
tldr: The Object.entries() method can be used to iterate over an object and apply a map function to each key/value pair.
---

**Contents**

[TOC]

### Object.keys

Object.keys() is a method that can be used to iterate over objects in Javascript. It takes an object as an argument and returns an array of the object's keys. This array can then be used in a for loop or with the Array.map() method to iterate over the object's keys and values.

### Array.map

Array.map() is a method that can be used to iterate over arrays in Javascript. It takes a callback function as an argument and returns a new array with the results of the callback function applied to each element in the array. This method can be used to iterate over an array of keys returned from Object.keys() and access the corresponding values in the object.

### Example

The following example demonstrates how Object.keys() and Array.map() can be used together to iterate over an object.

```javascript
const obj = {
  a: 1,
  b: 2,
  c: 3
};

const keys = Object.keys(obj);
const values = keys.map(key => obj[key]);

console.log(values); // [1, 2, 3]
```

In this example, Object.keys() is used to get an array of the object's keys, which is then used with Array.map() to access the corresponding values in the object. The result is an array of the object's values.
