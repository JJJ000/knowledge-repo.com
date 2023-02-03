---
title: What is the syntax for creating a two dimensional array in javascript?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-03 00:00:00
updated_at: 2023-02-03 00:00:00
tldr: You can create a two dimensional array in JavaScript by using the array literal notation with nested arrays.
---

**Contents**

[TOC]

**Creating a Two Dimensional Array**

1. Declare the Array: 
   To create a two-dimensional array in JavaScript, you must first declare the array with the `var` keyword. You can do this by assigning the array to a variable. For example: 
   ```
   var twoDimArray = [];
   ```

2. Create Inner Arrays: 
   To create the inner arrays, you can use the `push()` method to add elements to the array. For example:
   ```
   twoDimArray.push([1,2,3]);
   twoDimArray.push([4,5,6]);
   twoDimArray.push([7,8,9]);
   ```

3. Accessing Elements: 
   To access elements in the two-dimensional array, you can use the bracket notation. For example: 
   ```
   twoDimArray[0][2] // returns 3
   twoDimArray[1][1] // returns 5
   twoDimArray[2][0] // returns 7
   ```

4. Iterating Through the Array: 
   To iterate through the two-dimensional array, you can use nested `for` loops. For example: 
   ```
   for (let i = 0; i < twoDimArray.length; i++) {
      for (let j = 0; j < twoDimArray[i].length; j++) {
         console.log(twoDimArray[i][j]);
      }
   }
   ```
