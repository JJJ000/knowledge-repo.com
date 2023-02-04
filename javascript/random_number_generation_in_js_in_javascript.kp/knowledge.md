---
title: Initializing the random number generator in javascript
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-04 00:00:00
updated_at: 2023-02-04 00:00:00
tldr: Math.random() can be seeded using Math.seedrandom() with a specific seed value.
---

**Contents**

[TOC]

### Math.random()
Math.random() is a built-in function in JavaScript that generates a random number between 0 (inclusive) and 1 (exclusive). This function is not seeded and will produce the same sequence of numbers every time it is called.

### Math.seedrandom()
Math.seedrandom() is a library function that allows you to seed the random number generator. This function takes a seed value as an argument and uses it to generate a pseudo-random sequence of numbers.

### Usage
To use Math.seedrandom(), you must first include the library in your JavaScript code. You can then call the function with a seed value to generate a pseudo-random sequence of numbers.

### Example
```
// Include the library
<script src="seedrandom.js"></script>

// Generate a random number using a seed
var rand = Math.seedrandom(12345);
console.log(rand); // 0.4598989898989899
```
