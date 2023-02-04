---
title: What is the best way to randomize the order of items in an array?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-04 00:00:00
updated_at: 2023-02-04 00:00:00
tldr: To shuffle an array in Javascript, use the array`s sort() method with a random compare function.
---

**Contents**

[TOC]

#1 Using The Fisher-Yates Algorithm

The Fisher-Yates algorithm is a popular and efficient way to shuffle an array in Javascript. The algorithm works by looping through the array, picking a random element, and swapping it with the current element. The algorithm then continues looping through the array until it reaches the end.

#2 Implementing The Algorithm

To implement the Fisher-Yates algorithm in Javascript, you can use a for loop to iterate through the array and a Math.random() function to generate a random number. You can then use the random number to pick an element from the array and swap it with the current element.

#3 Example Code

Below is an example of how to implement the Fisher-Yates algorithm to shuffle an array in Javascript:

```
// Create an array
let arr = [1, 2, 3, 4, 5];

// Loop through the array
for (let i = arr.length - 1; i > 0; i--) {
  // Generate a random number
  let j = Math.floor(Math.random() * (i + 1));
  // Swap the current element with the random element
  let temp = arr[i];
  arr[i] = arr[j];
  arr[j] = temp;
}

// Shuffled array
console.log(arr);
```

#4 Conclusion

The Fisher-Yates algorithm is a popular and efficient way to shuffle an array in Javascript. It can be implemented using a for loop and a Math.random() function to generate a random number. The example code above shows how to implement the algorithm in Javascript.
