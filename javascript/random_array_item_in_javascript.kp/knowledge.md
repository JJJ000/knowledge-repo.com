---
title: Select a random element from a JavaScript array
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-03 00:00:00
updated_at: 2023-02-03 00:00:00
tldr: Math.random() can be used to generate a random number between 0 and 1, which can then be used to select a random item from an array.
---

**Contents**

[TOC]

##### Using Math.random()

Using the Math.random() method, you can get a random item from an array by generating a random number between 0 and the length of the array. The random number is then used to access the element at that index.

```javascript
let arr = ["apple", "banana", "orange", "watermelon"];

let randomItem = arr[Math.floor(Math.random() * arr.length)];

console.log(randomItem); // Outputs a random item from the array
```

##### Using Array.prototype.slice()

Using the Array.prototype.slice() method, you can create a shallow copy of the array and then use the Math.random() method to access a random item from the copied array.

```javascript
let arr = ["apple", "banana", "orange", "watermelon"];

let arrCopy = arr.slice();
let randomItem = arrCopy[Math.floor(Math.random() * arrCopy.length)];

console.log(randomItem); // Outputs a random item from the array
```

##### Using Lodash

You can also use the Lodash library to get a random item from an array. The Lodash _.sample() method takes an array as an argument and returns a random item from the array.

```javascript
let arr = ["apple", "banana", "orange", "watermelon"];

let randomItem = _.sample(arr);

console.log(randomItem); // Outputs a random item from the array
```
