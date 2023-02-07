---
title: What is the syntax for comparing two arrays in javascript?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: You can check if two arrays are equal by comparing their lengths and elements using the `Array.prototype.every()` method.
---

**Contents**

[TOC]

## Using the '==' Operator

The simplest way to check if two arrays are equal is to use the `==` operator. This operator checks for deep equality between two values, meaning it will check the elements of the array to determine if they are the same.

For example, the following code will return `true` if the two arrays are equal:

```
let arr1 = [1, 2, 3];
let arr2 = [1, 2, 3];

arr1 == arr2 // returns true
```

## Using the 'Object.is()' Method

Another way to check if two arrays are equal is to use the `Object.is()` method. This method checks for the same value equality between two values, meaning it will check if the elements of the array are the same and in the same order.

For example, the following code will return `true` if the two arrays are equal:

```
let arr1 = [1, 2, 3];
let arr2 = [1, 2, 3];

Object.is(arr1, arr2) // returns true
```

## Using the 'JSON.stringify()' Method

The `JSON.stringify()` method can also be used to check if two arrays are equal. This method converts a JavaScript object or value to a JSON string, which can then be compared to determine if the two arrays are equal.

For example, the following code will return `true` if the two arrays are equal:

```
let arr1 = [1, 2, 3];
let arr2 = [1, 2, 3];

JSON.stringify(arr1) === JSON.stringify(arr2) // returns true
```

## Using the 'Array.prototype.every()' Method

The `Array.prototype.every()` method can also be used to check if two arrays are equal. This method checks if all elements in an array pass a given test, which can be used to check if the two arrays are equal.

For example, the following code will return `true` if the two arrays are equal:

```
let arr1 = [1, 2, 3];
let arr2 = [1, 2, 3];

arr1.every((val, idx) => val === arr2[idx]) // returns true
```
