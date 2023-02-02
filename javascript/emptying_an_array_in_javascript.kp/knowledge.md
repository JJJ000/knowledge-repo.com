---
title: What is the best way to clear an array in javascript?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-02 00:00:00
updated_at: 2023-02-02 00:00:00
tldr: To empty an array in JavaScript, use the array`s `splice()` method with no arguments.
---

**Contents**

[TOC]

#1.Using the `length` Property: 

The simplest way to clear an array is to set its `length` property to 0. This will remove all elements from the array and will update its length to 0.

```
let array = [1, 2, 3, 4, 5];

array.length = 0;

console.log(array); // []
```

#2.Using the `splice()` Method:

The `splice()` method can be used to remove a range of elements from the array. This method takes two arguments, the starting index and the number of elements to remove.

```
let array = [1, 2, 3, 4, 5];

array.splice(0, array.length);

console.log(array); // []
```

#3.Using the `pop()` Method:

The `pop()` method can be used to remove the last element from the array. This method can be used in a loop to remove all elements from the array.

```
let array = [1, 2, 3, 4, 5];

while (array.length > 0) {
  array.pop();
}

console.log(array); // []
```

#4.Using the `shift()` Method:

The `shift()` method can be used to remove the first element from the array. This method can be used in a loop to remove all elements from the array.

```
let array = [1, 2, 3, 4, 5];

while (array.length > 0) {
  array.shift();
}

console.log(array); // []
```
