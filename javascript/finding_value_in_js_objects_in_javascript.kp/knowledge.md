---
title: Search for a value in a JavaScript array of objects
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-04 00:00:00
updated_at: 2023-02-04 00:00:00
tldr: Use the Array.prototype.find() method to find a value in an array of objects.
---

**Contents**

[TOC]

**Section 1: Finding a value in an array of objects**

To find a value in an array of objects, you can use the `find()` function. This function takes in a callback function as an argument and returns the first element in the array that satisfies the condition specified in the callback.

**Section 2: Syntax**

The syntax for the `find()` function is as follows:

`array.find(callback(element[, index[, array]])[, thisArg])`

**Section 3: Example**

For example, let's say we have an array of objects like this:

```
const array = [
  { id: 1, name: 'John' },
  { id: 2, name: 'Jane' },
  { id: 3, name: 'Bob' },
];
```

To find the object with the id of 2, we can use the `find()` function like this:

```
const result = array.find(obj => obj.id === 2);

console.log(result); // { id: 2, name: 'Jane' }
```

**Section 4: Conclusion**

In conclusion, the `find()` function is a useful tool for finding a value in an array of objects. It takes in a callback function as an argument, and returns the first element in the array that satisfies the condition specified in the callback.
