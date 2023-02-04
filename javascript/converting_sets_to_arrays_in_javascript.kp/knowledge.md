---
title: What is the process for converting a set to an array?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-03 00:00:00
updated_at: 2023-02-03 00:00:00
tldr: Use the spread operator (...) to convert a Set to an Array in Javascript.
---

**Contents**

[TOC]

### 1. Using Spread Operator

The spread operator (...) can be used to convert a Set to an Array.

```javascript
const mySet = new Set([1, 2, 3]);
const myArray = [...mySet];
console.log(myArray); // [1, 2, 3]
```

### 2. Using Array.from()

The Array.from() method can also be used to convert a Set to an Array.

```javascript
const mySet = new Set([1, 2, 3]);
const myArray = Array.from(mySet);
console.log(myArray); // [1, 2, 3]
```

### 3. Using for...of Loop

The for...of loop can be used to iterate over the Set and create a new Array.

```javascript
const mySet = new Set([1, 2, 3]);
const myArray = [];

for (let item of mySet) {
  myArray.push(item);
}

console.log(myArray); // [1, 2, 3]
```

### 4. Using forEach()

The forEach() method can also be used to iterate over the Set and create a new Array.

```javascript
const mySet = new Set([1, 2, 3]);
const myArray = [];

mySet.forEach(item => myArray.push(item));

console.log(myArray); // [1, 2, 3]
```
