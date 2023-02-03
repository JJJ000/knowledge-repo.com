---
title: Arrange the keys of a JavaScript object in order
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-03 00:00:00
updated_at: 2023-02-03 00:00:00
tldr: Use the Object.keys() method combined with the Array.sort() method to sort a JavaScript object by key.
---

**Contents**

[TOC]

### Solution 1:

Using the `Object.keys()` method and the `Array.sort()` method:

```javascript
let obj = {
    a: 1,
    b: 2,
    c: 3
};

let sortedObj = {};
let keys = Object.keys(obj).sort();
for (let key of keys) {
    sortedObj[key] = obj[key];
}
```

### Solution 2:

Using the `Object.entries()` method and the `Array.sort()` method:

```javascript
let obj = {
    a: 1,
    b: 2,
    c: 3
};

let sortedObj = {};
let entries = Object.entries(obj).sort((a, b) => a[0] > b[0]);
for (let entry of entries) {
    sortedObj[entry[0]] = entry[1];
}
```
