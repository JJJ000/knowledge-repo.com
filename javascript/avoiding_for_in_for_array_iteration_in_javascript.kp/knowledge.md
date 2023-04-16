---
title: What are the drawbacks of using "for...in" to iterate through an array?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Using `for...in` for array iteration is a bad idea in Javascript because it will also iterate over any additional properties added to the array.
---

**Contents**

[TOC]

### Unreliable Order
Using a `for...in` loop to iterate over an array can be unreliable because the order of the elements in the array is not guaranteed. Unlike a `for` loop, which guarantees that each element in the array will be visited in order, a `for...in` loop does not guarantee the order of the elements. This can lead to unintended results, as the code may not be expecting elements to be visited out of order.

### Poor Performance
Using a `for...in` loop to iterate over an array can also be inefficient, as the loop will have to check the index of each element in the array, which can be time-consuming. This can lead to poor performance in applications where speed is critical.

### Unintended Iteration
A `for...in` loop can also lead to unintended iteration, as the loop will also iterate over any properties that have been added to the array object itself. This can lead to unexpected results, as the loop will not only iterate over the elements in the array, but also any properties that have been added to the array object.

### Better Alternatives
Finally, there are better alternatives to using a `for...in` loop for array iteration. The `for` loop and the `forEach()` method are both more reliable and more efficient ways to iterate over an array. Both methods guarantee that the elements in the array will be visited in order, and both methods are more efficient than a `for...in` loop.
