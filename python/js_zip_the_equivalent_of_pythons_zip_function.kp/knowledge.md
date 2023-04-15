---
title: What is the js equivalent of python's zip function?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Javascript`s equivalent of Python`s zip function is the `map` method with the `spread operator.`
---

**Contents**

[TOC]

## Section 1: Introduction

Python's zip() function is a built-in function that takes multiple sequences and returns a list of tuples, where each tuple contains the corresponding elements from each sequence. This is a commonly used utility function in Python programming.

In this article, we will discuss the JavaScript equivalent of Python's zip() function.


## Section 2: Using the map() method

One way to implement zip() in JavaScript is to use the map() method. This method applies a provided function to each element of an array and returns a new array containing the results.

The idea is to take the first element of each input array and create a tuple (an array of two elements) from them. Then take the second element of each input array and create a second tuple, and so on.

Here's a sample implementation:

```javascript
function zip(...arrays) {
  const maxLength = Math.min(...arrays.map(arr => arr.length));
  return Array.from({ length: maxLength }).map((_, index) => {
    return Array.from({ length: arrays.length }, (_, i) => arrays[i][index]);
  });
}
```

This implementation uses the spread operator (...) to collect all input arrays. We then calculate the maximum length of these arrays and use it to initialize an array with that size. Finally, we use the map() method to transform this array into an array of tuples.


## Section 3: Using the reduce() method

Another way to implement zip() in JavaScript is to use the reduce() method. This method applies a provided function to each element of an array and returns a single value that accumulates the results.

The idea is to iterate over the first array and use its index to access the corresponding elements from the other arrays. We then create a tuple from these elements and add it to an accumulating array.

Here's a sample implementation:

```javascript
function zip(...arrays) {
  return arrays.reduce((acc, arr, i) => {
    arr.forEach((item, j) => {
      acc[j] = acc[j] || [];
      acc[j][i] = item;
    });
    return acc;
  }, []).map(item => item.filter(i => i !== undefined));
}
```

This implementation uses the reduce() method to iterate over the input arrays. We then use the forEach() method to iterate over each array element and create a tuple from them.

Finally, we use the map() method to remove any undefined values from the output arrays.


## Section 4: Conclusion

In this article, we discussed two ways to implement the Python zip() function in JavaScript. The first method uses the map() method to transform a flat array into an array of tuples. The second method uses the reduce() method to iterate over the input arrays and create tuples from their corresponding elements.

Both of these methods provide a way to transpose multiple arrays of equal length into an array of tuples.
