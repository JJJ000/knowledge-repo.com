---
title: Create an array with multiple copies of the same element
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-04 00:00:00
updated_at: 2023-02-04 00:00:00
tldr: You can create an array with same element repeated multiple times in Javascript by using the Array.from() method and passing in an array containing the element and the desired length.
---

**Contents**

[TOC]

### Creating Array

To create an array with same element repeated multiple times, we can use the `Array.from()` method. The `Array.from()` method takes two arguments: 

1. An array-like or iterable object to convert to an array. 
2. A map function to call on every element of the array, optional.

### Syntax

```
Array.from(arrayLike[, mapFn[, thisArg]])
```

### Example

Here is an example of creating an array with 3 elements of the same value:

```
const arr = Array.from({length: 3}, () => 'same element');
console.log(arr); // ["same element", "same element", "same element"]
```
