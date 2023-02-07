---
title: Create a copy of an array in reverse order without modifying the original array in javascript
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: Create a new array and use the Array.prototype.reverse() method to reverse the elements in the original array and assign them to the new array.
---

**Contents**

[TOC]

### Using `Array.prototype.slice()`

```javascript
const reverseArray = (arr) => arr.slice().reverse();
```

### Using `Array.prototype.reduce()`

```javascript
const reverseArray = (arr) => arr.reduce((acc, curr) => [curr, ...acc], []);
```

### Using `Array.prototype.map()`

```javascript
const reverseArray = (arr) => arr.map((e, i) => arr[arr.length - i - 1]);
```

### Using `Array.prototype.forEach()`

```javascript
const reverseArray = (arr) => {
  const reversed = [];
  arr.forEach((e, i) => reversed[i] = arr[arr.length - i - 1]);
  return reversed;
};
```
