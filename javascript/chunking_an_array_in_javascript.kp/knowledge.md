---
title: Divide array into sections
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-03 00:00:00
updated_at: 2023-02-03 00:00:00
tldr: Use the Array.prototype.slice() method to split an array into chunks.
---

**Contents**

[TOC]

## Using Array.prototype.slice()
The Array.prototype.slice() method can be used to split an array into chunks. It takes two arguments, the starting index and the ending index of the chunk.

```javascript
function chunkArray(arr, chunkSize) {
  const chunkedArray = [];

  for (let i = 0; i < arr.length; i += chunkSize) {
    const chunk = arr.slice(i, i + chunkSize);
    chunkedArray.push(chunk);
  }

  return chunkedArray;
}
```

## Using Array.prototype.splice()
The Array.prototype.splice() method can also be used to split an array into chunks. It takes three arguments, the starting index, the number of elements to be removed and the elements to be added.

```javascript
function chunkArray(arr, chunkSize) {
  const chunkedArray = [];

  while (arr.length > 0) {
    const chunk = arr.splice(0, chunkSize);
    chunkedArray.push(chunk);
  }

  return chunkedArray;
}
```

## Using Array.from()
The Array.from() method can be used to split an array into chunks. It takes two arguments, the array to be split and a map function which is used to transform the elements of the array.

```javascript
function chunkArray(arr, chunkSize) {
  const chunkedArray = Array.from(arr, (_, i) =>
    arr.slice(i * chunkSize, i * chunkSize + chunkSize)
  );

  return chunkedArray;
}
```

## Using forEach()
The forEach() method can be used to split an array into chunks. It takes a callback function as an argument which is used to transform the elements of the array.

```javascript
function chunkArray(arr, chunkSize) {
  const chunkedArray = [];

  arr.forEach((_, i) => {
    const chunk = arr.slice(i * chunkSize, i * chunkSize + chunkSize);
    chunkedArray.push(chunk);
  });

  return chunkedArray;
}
```
