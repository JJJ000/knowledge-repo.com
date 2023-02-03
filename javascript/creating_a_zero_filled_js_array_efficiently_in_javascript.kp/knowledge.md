---
title: What is the quickest way to make an array in JavaScript that is filled with zeroes?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-03 00:00:00
updated_at: 2023-02-03 00:00:00
tldr: The most efficient way to create a zero filled JavaScript array is to use the Array.from() method with a map() callback to fill each element with 0.
---

**Contents**

[TOC]

## Using Array.from
The most efficient way to create a zero filled JavaScript array is to use the `Array.from()` method. This method takes two arguments: an array-like object or iterable and a map function. The map function is used to fill the array with the desired values.

```
const arrayLength = 5;
const zeroFilledArray = Array.from({length: arrayLength}, () => 0);

// Output: [0, 0, 0, 0, 0]
```

## Using Array.fill
Another efficient way to create a zero filled JavaScript array is to use the `Array.fill()` method. This method takes in two arguments: the value to fill the array and the start index. By default, the start index is 0 and the value to fill the array with is 0.

```
const arrayLength = 5;
const zeroFilledArray = Array(arrayLength).fill(0);

// Output: [0, 0, 0, 0, 0]
```

## Using for loop
A third efficient way to create a zero filled JavaScript array is to use a for loop. This method takes in one argument: the length of the array.

```
const arrayLength = 5;
const zeroFilledArray = [];

for (let i = 0; i < arrayLength; i++) {
  zeroFilledArray.push(0);
}

// Output: [0, 0, 0, 0, 0]
```

## Using Array Spread Operator
A fourth efficient way to create a zero filled JavaScript array is to use the array spread operator. This method takes in one argument: the length of the array.

```
const arrayLength = 5;
const zeroFilledArray = [...Array(arrayLength)].fill(0);

// Output: [0, 0, 0, 0, 0]
```
