---
title: Access elements within the map() function
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-04 00:00:00
updated_at: 2023-02-04 00:00:00
tldr: The map() function calls a provided callback function once for each element in an array, in order, and returns an array containing the results. The callback is passed three arguments the current element being processed, the index of the current element, and the array over which it is iterating.
---

**Contents**

[TOC]

# Definition

Map() is a method in JavaScript that creates a new array with the results of calling a provided function on every element in the calling array.

# Syntax

The syntax for the map() method is as follows:

array.map(function(currentValue, index, arr), thisValue)

# Parameters

The map() method takes in two parameters:

- **currentValue**: The value of the current element being processed in the array.
- **index**: The index of the current element being processed in the array.

# Usage

The map() method is often used to iterate over an array and modify each element in the array. For example, the following code uses the map() method to double each element in the array:

```
let numbers = [1, 2, 3, 4, 5];
let doubledNumbers = numbers.map(number => number * 2);
console.log(doubledNumbers); // [2, 4, 6, 8, 10]
```
