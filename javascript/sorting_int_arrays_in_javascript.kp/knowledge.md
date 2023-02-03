---
title: What is the correct way to sort an array of integers?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-03 00:00:00
updated_at: 2023-02-03 00:00:00
tldr: Use the built-in Array.prototype.sort() method, passing in a comparison function if necessary.
---

**Contents**

[TOC]

# Sorting Algorithm

The most common sorting algorithm for sorting an array of integers is the **bubble sort** algorithm. This algorithm works by comparing adjacent elements of the array and swapping them if they are in the wrong order. This process is repeated until the array is fully sorted.

# Implementation

The following is a basic implementation of the bubble sort algorithm in JavaScript:

```javascript
function bubbleSort(arr) {
  let swapped;
  do {
    swapped = false;
    for (let i = 0; i < arr.length; i++) {
      if (arr[i] > arr[i + 1]) {
        let temp = arr[i];
        arr[i] = arr[i + 1];
        arr[i + 1] = temp;
        swapped = true;
      }
    }
  } while (swapped);
  return arr;
}
```

# Usage

The bubble sort algorithm can be used to sort an array of integers by passing the array to the function as an argument:

```javascript
let arr = [3, 8, 5, 2, 9, 1];
let sortedArr = bubbleSort(arr);
console.log(sortedArr); // [1, 2, 3, 5, 8, 9]
```

# Performance

The bubble sort algorithm has a time complexity of O(n^2), meaning that it is not very efficient for sorting large arrays. For large arrays, it is recommended to use a more efficient sorting algorithm such as quicksort or heapsort.
