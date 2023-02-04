---
title: Add a string to a certain position
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-04 00:00:00
updated_at: 2023-02-04 00:00:00
tldr: Use the splice() method to insert a string at a specific index in Javascript.
---

**Contents**

[TOC]

**Section 1: Using the splice() Method**

The splice() method can be used to insert a string at a specific index in Javascript. This method modifies the original array and also returns an array containing the deleted elements.

Syntax:
```javascript
array.splice(index, 0, item);
```

Parameters:
- index: The index at which the new item should be added.
- 0: This specifies that no item should be removed from the array.
- item: The item to be added to the array.

Example:
```javascript
var arr = ["a", "b", "c", "d"];
arr.splice(2, 0, "x");
// arr is now ["a", "b", "x", "c", "d"]
```

**Section 2: Using the slice() and concat() Methods**

The slice() and concat() methods can also be used to insert a string at a specific index in Javascript. This method does not modify the original array and instead creates a new array with the desired string inserted.

Syntax:
```javascript
var newArr = arr.slice(0, index).concat(item).concat(arr.slice(index));
```

Parameters:
- arr: The original array.
- index: The index at which the new item should be added.
- item: The item to be added to the array.

Example:
```javascript
var arr = ["a", "b", "c", "d"];
var newArr = arr.slice(0, 2).concat("x").concat(arr.slice(2));
// newArr is now ["a", "b", "x", "c", "d"]
```

**Section 3: Using the spread operator**

The spread operator can also be used to insert a string at a specific index in Javascript. This method does not modify the original array and instead creates a new array with the desired string inserted.

Syntax:
```javascript
var newArr = [...arr.slice(0, index), item, ...arr.slice(index)];
```

Parameters:
- arr: The original array.
- index: The index at which the new item should be added.
- item: The item to be added to the array.

Example:
```javascript
var arr = ["a", "b", "c", "d"];
var newArr = [...arr.slice(0, 2), "x", ...arr.slice(2)];
// newArr is now ["a", "b", "x", "c", "d"]
```

**Section 4: Using the Array.from() Method**

The Array.from() method can also be used to insert a string at a specific index in Javascript. This method does not modify the original array and instead creates a new array with the desired string inserted.

Syntax:
```javascript
var newArr = Array.from(arr, (x, i) => i === index ? item : x);
```

Parameters:
- arr: The original array.
- index: The index at which the new item should be added.
- item: The item to be added to the array.

Example:
```javascript
var arr = ["a", "b", "c", "d"];
var newArr = Array.from(arr, (x, i) => i === 2 ? "x" : x);
// newArr is now ["a", "b", "x", "c", "d"]
```
