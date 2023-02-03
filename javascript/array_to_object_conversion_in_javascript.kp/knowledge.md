---
title: Transform array into object
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-03 00:00:00
updated_at: 2023-02-03 00:00:00
tldr: Use the Array.reduce() method to convert an array to an object in JavaScript.
---

**Contents**

[TOC]

## Solution 1
Using `Object.assign()`:

```javascript
const array = [1, 2, 3, 4];
const object = Object.assign({}, array);
```

## Solution 2
Using `Array.reduce()`:

```javascript
const array = [1, 2, 3, 4];
const object = array.reduce((obj, item) => {
  obj[item] = item;
  return obj;
}, {});
```

## Solution 3
Using `for...of` loop:

```javascript
const array = [1, 2, 3, 4];
const object = {};
for (let item of array) {
  object[item] = item;
}
```

## Solution 4
Using `forEach()` loop:

```javascript
const array = [1, 2, 3, 4];
const object = {};
array.forEach(item => {
  object[item] = item;
});
```
