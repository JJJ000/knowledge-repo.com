---
title: Exchange JavaScript array elements
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-08 00:00:00
updated_at: 2023-02-08 00:00:00
tldr: To swap two elements in an array, use the array indexing syntax to assign the values of the two elements to each other.
---

**Contents**

[TOC]

# Section 1: Introduction

Swapping array elements is a common task in programming. It involves exchanging the values of two array elements, usually with the help of a temporary variable. This article will explain how to swap array elements using JavaScript.

# Section 2: The Code

The code for swapping array elements in JavaScript is as follows:

```javascript
// Define the two elements to swap
let a = [1,2,3];
let b = [4,5,6];

// Create a temporary variable to store one of the values
let temp = a;

// Swap the values
a = b;
b = temp;

// Output the swapped values
console.log(a); // [4,5,6]
console.log(b); // [1,2,3]
```

# Section 3: Explanation

The code first defines two arrays, `a` and `b`, which contain the values to be swapped. It then creates a temporary variable, `temp`, and assigns it the value of `a`. This ensures that the value of `a` is not lost during the swap. 

The code then swaps the values of `a` and `b` by assigning the value of `b` to `a` and the value of `temp` (which is the original value of `a`) to `b`.

Finally, the code prints the swapped values of `a` and `b` to the console.

# Section 4: Conclusion

Swapping array elements in JavaScript is a simple task that can be achieved with just a few lines of code. By following the steps outlined above, you can easily swap the values of two array elements.
