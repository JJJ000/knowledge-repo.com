---
title: What is the procedure for determining if an array is empty or has elements?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-04 00:00:00
updated_at: 2023-02-04 00:00:00
tldr: To check if an array is empty or exists in Javascript, use the Array.isArray() method.
---

**Contents**

[TOC]

#1 Checking if an Array is Empty

To check if an array is empty or not, you can use the `length` property of the array. If the `length` property is equal to 0, then the array is empty.

```
let myArray = [];

if (myArray.length === 0) {
  console.log('Array is empty');
}
```

#2 Checking if an Array Exists

To check if an array exists, you can use the `typeof` operator. If the `typeof` operator returns `object`, then the array exists.

```
let myArray = [];

if (typeof myArray === 'object') {
  console.log('Array exists');
}
```
