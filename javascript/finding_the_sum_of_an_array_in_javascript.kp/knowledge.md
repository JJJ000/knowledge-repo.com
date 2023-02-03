---
title: What is the total of an array of numbers?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-03 00:00:00
updated_at: 2023-02-03 00:00:00
tldr: The sum of an array of numbers in Javascript can be found by using the reduce() method.
---

**Contents**

[TOC]

## Using a Loop

1. Create a variable to store the sum and initialize it to 0.

```javascript
let sum = 0;
```

2. Loop through the array of numbers and add each number to the sum.

```javascript
for (let i = 0; i < array.length; i++) {
 sum += array[i];
}
```

3. Return the sum.

```javascript
return sum;
```

## Using the Reduce Method

1. Create a function that takes an array of numbers as an argument.

```javascript
function sumArray(array) {
```

2. Use the reduce() method to add the numbers in the array and store the result in a variable.

```javascript
let sum = array.reduce((acc, cur) => acc + cur);
```

3. Return the sum.

```javascript
return sum;
```

4. Call the function with the array of numbers as an argument.

```javascript
sumArray(array);
```
