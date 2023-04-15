---
title: What is the best way to determine if an object is an array?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-04-17 00:00:00
updated_at: 2023-04-17 00:00:00
tldr: You can check if an object is an array in Javascript by using the Array.isArray() method.
---

**Contents**

[TOC]

### Using `Array.isArray`

The `Array.isArray()` method can be used to check if an object is an array. This method returns `true` if the object is an array, and `false` otherwise.

```
var arr = [1, 2, 3];
Array.isArray(arr); // returns true

var obj = {name: 'John'};
Array.isArray(obj); // returns false
```

### Using `instanceof`

The `instanceof` operator can also be used to check if an object is an array. This operator returns `true` if the object is an instance of the specified constructor.

```
var arr = [1, 2, 3];
arr instanceof Array; // returns true

var obj = {name: 'John'};
obj instanceof Array; // returns false
```

### Using `typeof`

The `typeof` operator can also be used to check if an object is an array. This operator returns `object` if the object is an array, and `other type` otherwise.

```
var arr = [1, 2, 3];
typeof arr; // returns 'object'

var obj = {name: 'John'};
typeof obj; // returns 'object'
```

### Using `Object.prototype.toString`

The `Object.prototype.toString()` method can also be used to check if an object is an array. This method returns `[object Array]` if the object is an array, and `[object Object]` otherwise.

```
var arr = [1, 2, 3];
Object.prototype.toString.call(arr); // returns '[object Array]'

var obj = {name: 'John'};
Object.prototype.toString.call(obj); // returns '[object Object]'
```
