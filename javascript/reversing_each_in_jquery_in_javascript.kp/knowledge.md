---
title: Each() .jquery
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: In JavaScript, you can loop through an array in reverse order using the for loop with a decrementing counter.
---

**Contents**

[TOC]

# For Loop 
The most common way to iterate over an array in reverse is to use a `for` loop. This loop starts at the last index of the array and decrements the index by one until it reaches the beginning of the array.

```
for (let i = arr.length - 1; i >= 0; i--) {
  console.log(arr[i]);
}
```

# While Loop
Another option is to use a `while` loop. This loop checks if the index is greater than or equal to 0 and decrements the index by one until it reaches the beginning of the array.

```
let i = arr.length - 1;
while (i >= 0) {
  console.log(arr[i]);
  i--;
}
```

# Array.prototype.forEach()
The `Array.prototype.forEach()` method can also be used to iterate over an array in reverse. This method takes a callback function as an argument, which is called with each element in the array. The callback function can be used to decrement the index by one until it reaches the beginning of the array.

```
let i = arr.length - 1;
arr.forEach(() => {
  console.log(arr[i]);
  i--;
});
```

# Array.prototype.reduceRight()
The `Array.prototype.reduceRight()` method can also be used to iterate over an array in reverse. This method takes a callback function as an argument, which is called with each element in the array. The callback function can be used to decrement the index by one until it reaches the beginning of the array.

```
arr.reduceRight((acc, curr) => {
  console.log(curr);
  return acc - 1;
}, arr.length - 1);
```
