---
title: Searching an element in a JSON array using an index
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-10 00:00:00
updated_at: 2023-02-10 00:00:00
tldr: The indexOf() method can be used to find an element in a JSON array.
---

**Contents**

[TOC]

## Using `for` loop

We can use a `for` loop to iterate over the JSON array and compare each element with the value we are looking for. If the element matches the value, we can return its index.

```js
function getIndex(arr, val) {
  for (let i = 0; i < arr.length; i++) {
    if (arr[i] === val) {
      return i;
    }
  }
  return -1;
}
```

## Using `Array.prototype.findIndex()`

We can use the `Array.prototype.findIndex()` method to find the index of the element in the array. This method takes a function as a parameter which is used to test each element of the array. If the function returns `true`, the index of the element is returned.

```js
function getIndex(arr, val) {
  return arr.findIndex(el => el === val);
}
```

## Using `Array.prototype.indexOf()`

We can use the `Array.prototype.indexOf()` method to find the index of the element in the array. This method takes the element we are looking for as a parameter and returns its index if found.

```js
function getIndex(arr, val) {
  return arr.indexOf(val);
}
```

## Using `Array.prototype.find()`

We can use the `Array.prototype.find()` method to find the element in the array. This method takes a function as a parameter which is used to test each element of the array. If the function returns `true`, the element is returned. We can then use the `Array.prototype.indexOf()` method to get the index of the element.

```js
function getIndex(arr, val) {
  const el = arr.find(el => el === val);
  return arr.indexOf(el);
}
```
