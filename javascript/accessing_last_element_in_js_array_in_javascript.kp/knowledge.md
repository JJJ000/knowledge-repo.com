---
title: Retrieving the final element in a JavaScript array
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-03 00:00:00
updated_at: 2023-02-03 00:00:00
tldr: The last element of an array can be accessed using the index of the array length minus one.
---

**Contents**

[TOC]

# Using Array.prototype.pop()
The `Array.prototype.pop()` method is used to remove the last element of an array and return that element.

Syntax:
```
arr.pop()
```

Example:
```
let fruits = ["Banana", "Orange", "Apple", "Mango"];
let lastElement = fruits.pop();

// fruits is now ["Banana", "Orange", "Apple"]
// lastElement is "Mango"
```

# Using Array.length
The `Array.length` property can be used to access the last element of an array.

Syntax:
```
arr[arr.length-1]
```

Example:
```
let fruits = ["Banana", "Orange", "Apple", "Mango"];
let lastElement = fruits[fruits.length-1];

// fruits is still ["Banana", "Orange", "Apple", "Mango"]
// lastElement is "Mango"
```
