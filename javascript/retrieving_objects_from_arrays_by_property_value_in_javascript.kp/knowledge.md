---
title: Retrieve a JavaScript object from an array of objects based on the value of a property
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-03 00:00:00
updated_at: 2023-02-03 00:00:00
tldr: Use the Array.prototype.find() method to get the JavaScript object from an array of objects by value of property.
---

**Contents**

[TOC]

**Section 1: Introduction**

JavaScript objects can be accessed from an array of objects by value of property. This can be done using the `find()` method or `forEach()` loop. In this article, we will explain how to get a JavaScript object from an array of objects by value of property.

**Section 2: Using the find() Method**

The `find()` method is used to get the value of the first element in the array that satisfies the provided condition. This method takes a callback function as its argument and returns the value of the first element in the array that satisfies the condition. The syntax of the `find()` method is as follows:

```
array.find(callback(element[, index[, array]]) [, thisArg])
```

The `callback` function takes three arguments: `element`, `index`, and `array`. The `element` argument represents the current element being processed in the array. The `index` argument represents the index of the current element being processed in the array. The `array` argument represents the array being processed.

**Section 3: Using the forEach() Loop**

The `forEach()` loop is used to iterate over an array and perform a given operation on each element of the array. This loop takes a callback function as its argument and executes the callback function for each element of the array. The syntax of the `forEach()` loop is as follows:

```
array.forEach(callback(currentValue[, index[, array]]) [, thisArg])
```

The `callback` function takes three arguments: `currentValue`, `index`, and `array`. The `currentValue` argument represents the current element being processed in the array. The `index` argument represents the index of the current element being processed in the array. The `array` argument represents the array being processed.

**Section 4: Conclusion**

In this article, we have discussed how to get a JavaScript object from an array of objects by value of property. We have seen that this can be done using the `find()` method or `forEach()` loop. Both methods take a callback function as their argument and return the value of the first element in the array that satisfies the condition.
