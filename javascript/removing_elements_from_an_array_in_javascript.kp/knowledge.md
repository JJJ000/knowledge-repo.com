---
title: What is the most efficient way to delete an item from an array in javascript?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: Use the Array.prototype.splice() method to remove an element from an array in JavaScript.
---

**Contents**

[TOC]

#1 Removing an Element from the End of an Array

The `pop()` method can be used to remove the last element from an array. This method modifies the array by removing the last element and returns the removed element.

#2 Removing an Element from the Beginning of an Array

The `shift()` method can be used to remove the first element from an array. This method modifies the array by removing the first element and returns the removed element.

#3 Removing an Element from the Middle of an Array

The `splice()` method can be used to remove an element from an array. This method takes two arguments: the index of the element to be removed and the number of elements to be removed. This method modifies the array by removing the specified element and returns the removed element.

#4 Removing an Element from an Array Based on a Condition

The `filter()` method can be used to remove an element from an array based on a condition. This method takes a callback function as an argument and returns a new array with the elements that pass the condition.
