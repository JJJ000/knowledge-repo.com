---
title: Check if an array includes a certain value
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-03 00:00:00
updated_at: 2023-02-03 00:00:00
tldr: The Array.prototype.includes() method can be used to determine if an array contains a specified value.
---

**Contents**

[TOC]

**Section 1: Using Array.prototype.includes()**

The Array.prototype.includes() method can be used to determine whether an array contains a certain value. This method takes in the value to search for as its argument and returns a boolean value of true if the value is found in the array, or false if it is not.

**Section 2: Using Array.prototype.indexOf()**

The Array.prototype.indexOf() method can also be used to determine whether an array contains a certain value. This method takes in the value to search for as its argument and returns the index of the value in the array if it is found, or -1 if it is not.

**Section 3: Using Array.prototype.some()**

The Array.prototype.some() method can also be used to determine whether an array contains a certain value. This method takes in a callback function as its argument, which should return true if the value is found in the array, or false if it is not.

**Section 4: Using a for loop**

A for loop can also be used to determine whether an array contains a certain value. This loop should iterate through the array, checking each value to see if it is equal to the value being searched for. If the value is found, the loop should break and return true. If the value is not found, the loop should return false.
