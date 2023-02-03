---
title: Selecting a random element from a JavaScript array
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-03 00:00:00
updated_at: 2023-02-03 00:00:00
tldr: Use the array`s built-in method .random() to get a random value from the array.
---

**Contents**

[TOC]

1. Accessing a Random Value from an Array
----------------------------------------
The most common way to get a random value from an array is to use the `Math.random()` method. This method returns a random number between 0 and 1. We can use this number to select an element from an array.

2. Using Math.random() to Access an Array
----------------------------------------
We can use the `Math.random()` method to access an array by multiplying the random number by the array length and then using the `Math.floor()` method to round the number down to the nearest integer. This integer can be used as an index to access elements from the array.

3. Example
----------
For example, if we have an array with three elements, we can use the following code to get a random element from the array:

```
var myArray = [1, 2, 3];

// Get a random number between 0 and 1
var randomNumber = Math.random();

// Multiply the random number by the array length
var randomIndex = randomNumber * myArray.length;

// Round the number down to the nearest integer
var randomIndex = Math.floor(randomIndex);

// Get the element at the random index
var randomElement = myArray[randomIndex];
```

4. Conclusion
-------------
By using the `Math.random()` and `Math.floor()` methods, we can access a random element from an array in JavaScript.
