---
title: Check if a nested JavaScript object has a certain key
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-03 00:00:00
updated_at: 2023-02-03 00:00:00
tldr: You can use the `in` operator to test for the existence of a nested JavaScript object key.
---

**Contents**

[TOC]

**Using the 'in' Operator**

The 'in' operator can be used to test for the existence of a nested JavaScript object key. The syntax for this is `key in object`. This will return a boolean value of true if the key exists, and false if it does not.

**Example**

```
let obj = {
  a: {
    b: 'c'
  }
}

console.log('a' in obj); // true
console.log('b' in obj); // false
```

**Using the 'hasOwnProperty' Method**

The 'hasOwnProperty' method can be used to test for the existence of a nested JavaScript object key. The syntax for this is `object.hasOwnProperty(key)`. This will return a boolean value of true if the key exists, and false if it does not.

**Example**

```
let obj = {
  a: {
    b: 'c'
  }
}

console.log(obj.hasOwnProperty('a')); // true
console.log(obj.hasOwnProperty('b')); // false
```
