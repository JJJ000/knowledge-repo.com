---
title: Arrange elements of a JavaScript array in accordance with the order of another array
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: You can use the Array.prototype.sort() method and pass in a custom comparator function to sort an array based on another array.
---

**Contents**

[TOC]

**Section 1: Overview**

Javascript provides a variety of methods for sorting an array based on another array. The most common approach is to use the `sort()` method, which takes a comparison function as an argument. This comparison function can be used to compare elements in the two arrays and sort the original array accordingly.

**Section 2: Using the sort() Method**

The `sort()` method can be used to sort an array based on a comparison function. This comparison function takes two elements from the original array as arguments and returns a number that represents how the two elements should be sorted relative to each other. By using this comparison function, the `sort()` method can be used to sort the original array based on the elements of another array.

**Section 3: Example Code**

The following example shows how the `sort()` method can be used to sort an array based on another array. In this example, the `originalArray` is sorted based on the values in the `sortArray`.

```javascript
let originalArray = [5, 6, 3, 4, 1, 2];
let sortArray = [2, 3, 1, 4, 5, 6];

originalArray.sort((a, b) => {
  let indexA = sortArray.indexOf(a);
  let indexB = sortArray.indexOf(b);
  return indexA - indexB;
});

console.log(originalArray); // [2, 3, 1, 4, 5, 6]
```

**Section 4: Conclusion**

In conclusion, Javascript provides a variety of methods for sorting an array based on another array. The most common approach is to use the `sort()` method, which takes a comparison function as an argument. This comparison function can be used to compare elements in the two arrays and sort the original array accordingly.
