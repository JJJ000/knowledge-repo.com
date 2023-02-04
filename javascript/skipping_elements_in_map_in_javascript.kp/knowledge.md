---
title: What is the syntax for skipping an element when using .map()?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-03 00:00:00
updated_at: 2023-02-03 00:00:00
tldr: You can use the Array.prototype.filter() method to filter out the element you want to skip over before mapping.
---

**Contents**

[TOC]

### Using .filter()

The .filter() method can be used to skip over an element in .map() by filtering out the elements that you do not want to include in the .map() output. This is done by returning a boolean value of false for the element that is to be filtered out.

### Example

For example, let's say we have an array of numbers and we want to map each number to its square, but skip over the number 7. We can do this by using the .filter() method within the .map() method.

```
const numbers = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10];

const squares = numbers.map(num => num * num).filter(num => num !== 49);

console.log(squares); // [1, 4, 9, 16, 25, 36, 64, 81, 100]
```

### Alternative

An alternative way to skip over an element in .map() is to use the ternary operator within the .map() method. The ternary operator checks a condition and if it is true, the expression before the colon is returned, and if it is false, the expression after the colon is returned.

### Example

For example, let's say we have an array of numbers and we want to map each number to its square, but skip over the number 7. We can do this by using the ternary operator within the .map() method.

```
const numbers = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10];

const squares = numbers.map(num => num === 7 ? num : num * num);

console.log(squares); // [1, 4, 9, 16, 25, 36, 7, 64, 81, 100]
```
