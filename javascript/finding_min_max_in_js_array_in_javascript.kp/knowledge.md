---
title: Determine the smallest/largest value in an array using javascript
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-03 00:00:00
updated_at: 2023-02-03 00:00:00
tldr: The min/max element of an array in JavaScript can be found using the Math.min() and Math.max() methods.
---

**Contents**

[TOC]

## Using Math.min() and Math.max()

The Math.min() and Math.max() methods can be used to find the minimum and maximum elements of an array in JavaScript.

Syntax:

```
Math.min(array[, value1[, value2[, ...]]])
Math.max(array[, value1[, value2[, ...]]])
```

Example:

```
var numbers = [5, 6, 2, 3, 7];

// Get the minimum value in the array
var min = Math.min(...numbers);

// Get the maximum value in the array
var max = Math.max(...numbers);

console.log(min); // 2
console.log(max); // 7
```

## Using for loop

We can also use a for loop to find the min and max element of an array.

Syntax:

```
for (let i = 0; i < array.length; i++) {
  // code to find min and max
}
```

Example:

```
var numbers = [5, 6, 2, 3, 7];

// Initialize min and max variables
var min = numbers[0];
var max = numbers[0];

for (let i = 0; i < numbers.length; i++) {
  if (numbers[i] < min) {
    min = numbers[i];
  }
  if (numbers[i] > max) {
    max = numbers[i];
  }
}

console.log(min); // 2
console.log(max); // 7
```

## Using reduce()

The reduce() method can also be used to find the min and max elements of an array.

Syntax:

```
array.reduce(function(accumulator, currentValue) {
  // code to find min and max
}, initialValue);
```

Example:

```
var numbers = [5, 6, 2, 3, 7];

// Find the minimum value in the array
var min = numbers.reduce(function(a, b) {
  return Math.min(a, b);
});

// Find the maximum value in the array
var max = numbers.reduce(function(a, b) {
  return Math.max(a, b);
});

console.log(min); // 2
console.log(max); // 7
```
