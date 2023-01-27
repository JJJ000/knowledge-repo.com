---
title: What is the best way to take out a particular element from an array?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-01-27 00:00:00
updated_at: 2023-01-27 00:00:00
tldr: Use the `splice()` method to remove a specific item from an array in JavaScript.
---

**Contents**

[TOC]

**Using `splice()`**

`splice()` is a method used to remove elements from an array. It takes two arguments: the index of the element to remove, and the number of elements to remove.

**Syntax**

```
array.splice(index, howMany)
```

**Example**

```javascript
var arr = [1, 2, 3, 4, 5];
arr.splice(2, 1);
// arr is now [1, 2, 4, 5]
```

**Using `filter()`**

`filter()` is a method used to create a new array with elements that pass a certain condition. It takes a callback function which is used to test each element of the array, and returns a new array with elements that pass the test.

**Syntax**

```javascript
array.filter(function(element, index, array))
```

**Example**

```javascript
var arr = [1, 2, 3, 4, 5];
var newArr = arr.filter(function(element) {
  return element !== 3;
});
// newArr is now [1, 2, 4, 5]
```
