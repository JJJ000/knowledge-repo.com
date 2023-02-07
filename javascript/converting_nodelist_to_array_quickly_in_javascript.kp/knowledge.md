---
title: What is the quickest method for transforming a JavaScript nodelist into an array?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: The fastest way to convert a JavaScript NodeList to an Array is to use the Array.from() method.
---

**Contents**

[TOC]

### Method 1: Array.from()
The Array.from() method creates a new, shallow-copied Array instance from an array-like or iterable object.

Syntax:

```
Array.from(nodeList)
```

Example:

```
let nodeList = document.querySelectorAll('div');
let array = Array.from(nodeList);
```

### Method 2: Spread Operator
The spread operator (...) expands an iterable object into its elements.

Syntax:

```
[...nodeList]
```

Example:

```
let nodeList = document.querySelectorAll('div');
let array = [...nodeList];
```

### Method 3: Array.prototype.slice.call()
The Array.prototype.slice.call() method calls a function with a given this value and arguments provided individually.

Syntax:

```
Array.prototype.slice.call(nodeList)
```

Example:

```
let nodeList = document.querySelectorAll('div');
let array = Array.prototype.slice.call(nodeList);
```

### Method 4: for loop
A for loop is a type of loop that iterates through a set of values, executing a block of code for each value.

Syntax:

```
let array = [];
for (let i = 0; i < nodeList.length; i++) {
  array.push(nodeList[i]);
}
```

Example:

```
let nodeList = document.querySelectorAll('div');
let array = [];
for (let i = 0; i < nodeList.length; i++) {
  array.push(nodeList[i]);
}
```
