---
title: Organize a JSON object using javascript
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-18 00:00:00
updated_at: 2023-02-18 00:00:00
tldr: Objects can be sorted in JavaScript by using the sort() method on an array containing the Object keys.
---

**Contents**

[TOC]

### Sort By Key

To sort a JSON object by key, you can use the `Object.keys()` and `Array.prototype.sort()` methods. The `Object.keys()` method returns an array of the object's own enumerable property names, in the same order as we get with a normal loop. The `Array.prototype.sort()` method sorts the array in alphabetical order.

```javascript
let obj = {
  "c": 3,
  "b": 2,
  "a": 1
};

let keys = Object.keys(obj);
keys.sort();

let sortedObj = {};

keys.forEach(function(key) {
  sortedObj[key] = obj[key];
});

console.log(sortedObj);
// {a: 1, b: 2, c: 3}
```

### Sort By Value

To sort a JSON object by value, you can use the `Object.entries()` and `Array.prototype.sort()` methods. The `Object.entries()` method returns an array of the object's own enumerable property [key, value] pairs, in the same order as we get with a normal loop. The `Array.prototype.sort()` method sorts the array in ascending order.

```javascript
let obj = {
  "c": 3,
  "b": 2,
  "a": 1
};

let entries = Object.entries(obj);
entries.sort((a, b) => a[1] - b[1]);

let sortedObj = {};

entries.forEach(entry => {
  sortedObj[entry[0]] = entry[1];
});

console.log(sortedObj);
// {a: 1, b: 2, c: 3}
```

### Sort By Custom Logic

To sort a JSON object by custom logic, you can use the `Object.entries()` and `Array.prototype.sort()` methods. The `Object.entries()` method returns an array of the object's own enumerable property [key, value] pairs, in the same order as we get with a normal loop. The `Array.prototype.sort()` method sorts the array according to the provided compare function.

```javascript
let obj = {
  "c": 3,
  "b": 2,
  "a": 1
};

let entries = Object.entries(obj);
entries.sort((a, b) => {
  if (a[1] > b[1]) return -1;
  if (a[1] < b[1]) return 1;
  return 0;
});

let sortedObj = {};

entries.forEach(entry => {
  sortedObj[entry[0]] = entry[1];
});

console.log(sortedObj);
// {c: 3, b: 2, a: 1}
```
