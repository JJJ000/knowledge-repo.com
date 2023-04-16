---
title: What is the procedure for determining if an array is empty or does not exist?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Use the `Array.isArray()` method to check if an array exists, and the `Array.length` property to check if it is empty.
---

**Contents**

[TOC]

## Option 1: Using the Length Property

If we are dealing with an array, we can use the `length` property to check if the array is empty. The `length` property returns the number of elements in an array. If the array is empty, the `length` property will return 0. 

```javascript
const arr = [];
if (arr.length === 0) {
  console.log('Array is empty');
}
```

## Option 2: Using the Every Method

The `every()` method takes a callback function as an argument and returns a boolean value. If the callback function returns true for every element in the array, the `every()` method will return true. We can use this method to check if an array is empty by providing an empty callback function.

```javascript
const arr = [];
if (arr.every(() => true)) {
  console.log('Array is empty');
}
```

## Option 3: Using the Some Method

The `some()` method is similar to the `every()` method. It takes a callback function as an argument and returns a boolean value. If the callback function returns true for any element in the array, the `some()` method will return true. We can use this method to check if an array is empty by providing an empty callback function.

```javascript
const arr = [];
if (!arr.some(() => true)) {
  console.log('Array is empty');
}
```

## Option 4: Using the Typeof Operator

We can use the `typeof` operator to check if an array is empty or does not exist. If the array does not exist, the `typeof` operator will return `undefined`. If the array is empty, the `typeof` operator will return `object`.

```javascript
const arr = [];
if (typeof arr === 'undefined' || typeof arr === 'object') {
  console.log('Array is empty or does not exist');
}
```
