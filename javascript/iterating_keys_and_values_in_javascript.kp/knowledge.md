---
title: What is the process for looping through (keys, values) in javascript?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-04 00:00:00
updated_at: 2023-02-04 00:00:00
tldr: You can use the for-in loop to iterate over the keys, and the for-of loop to iterate over the values.
---

**Contents**

[TOC]

**Iterating Keys**

1. Using a `for...in` loop: 
```javascript
let obj = {a: 1, b: 2, c: 3};

for (let key in obj) {
  console.log(key); // Output: a, b, c
}
```

2. Using `Object.keys()`: 
```javascript
let obj = {a: 1, b: 2, c: 3};

Object.keys(obj).forEach(function(key) {
  console.log(key); // Output: a, b, c
});
```

**Iterating Values**

1. Using a `for...in` loop: 
```javascript
let obj = {a: 1, b: 2, c: 3};

for (let key in obj) {
  console.log(obj[key]); // Output: 1, 2, 3
}
```

2. Using `Object.values()`: 
```javascript
let obj = {a: 1, b: 2, c: 3};

Object.values(obj).forEach(function(value) {
  console.log(value); // Output: 1, 2, 3
});
```
