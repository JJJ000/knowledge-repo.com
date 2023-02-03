---
title: What is the most efficient method of determining if an item is present in a JavaScript array?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-03 00:00:00
updated_at: 2023-02-03 00:00:00
tldr: The best way to find if an item is in a JavaScript array is to use the Array.prototype.includes() method.
---

**Contents**

[TOC]

1. Using `Array.includes()` 
    - `Array.includes()` is a method that can be used to determine whether an array includes a certain value among its entries. 
    - It returns a boolean value of either `true` or `false`, depending on the presence of the value in the array.
    - Syntax: `array.includes(valueToFind[, fromIndex])`

2. Using `Array.indexOf()`
    - `Array.indexOf()` is a method that can be used to find the position of the first occurrence of a specified value in an array.
    - It returns the index of the element in the array, or `-1` if the element is not present.
    - Syntax: `array.indexOf(valueToFind[, fromIndex])`

3. Using `Array.some()`
    - `Array.some()` is a method that tests whether at least one element in the array passes the test implemented by the provided function.
    - It returns a boolean value of either `true` or `false`, depending on the presence of the value in the array.
    - Syntax: `array.some(function(currentValue[, index[, array]]) {
    // returns a boolean
    }[, thisArg])`

4. Using `Array.find()`
    - `Array.find()` is a method that returns the value of the first element in the array that satisfies the provided testing function.
    - It returns the value of the element in the array, or `undefined` if the element is not present.
    - Syntax: `array.find(function(currentValue[, index[, array]]) {
    // returns a boolean
    }[, thisArg])`
