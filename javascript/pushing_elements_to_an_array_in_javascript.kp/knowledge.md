---
title: Add multiple items to an array
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: You can use the Array.prototype.push() method to push multiple elements to an array in Javascript.
---

**Contents**

[TOC]

### Using the push() Method

The `push()` method is used to add one or more elements to the end of an array and returns the new length of the array.

Syntax:

```
array.push(element1[, ...[, elementN]])
```

Example:

```
var fruits = ["Apple", "Banana"];
fruits.push("Orange", "Kiwi");

console.log(fruits);
// Output: ["Apple", "Banana", "Orange", "Kiwi"]
```

### Using the spread Operator

The spread operator (`...`) can be used to add multiple elements to the end of an array.

Syntax:

```
[...array, element1[, ...[, elementN]]]
```

Example:

```
var fruits = ["Apple", "Banana"];
fruits = [...fruits, "Orange", "Kiwi"];

console.log(fruits);
// Output: ["Apple", "Banana", "Orange", "Kiwi"]
```

### Using the concat() Method

The `concat()` method is used to merge two or more arrays. This method does not change the existing arrays, but instead returns a new array.

Syntax:

```
array1.concat(array2[, array3, ..., arrayN])
```

Example:

```
var fruits1 = ["Apple", "Banana"];
var fruits2 = ["Orange", "Kiwi"];
var fruits = fruits1.concat(fruits2);

console.log(fruits);
// Output: ["Apple", "Banana", "Orange", "Kiwi"]
```
