---
title: What is the syntax for determining if a given string is present in an array in javascript/jquery?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Use the Array.prototype.includes() method to check if an array contains a specific string.
---

**Contents**

[TOC]

**Section 1: Using the `Array.includes()` Method**

The `Array.includes()` method can be used to check if an array contains a specific string. It returns a boolean value (`true` or `false`) depending on whether the array contains the specified string or not.

**Section 2: Using a `for` Loop**

A `for` loop can also be used to check if an array contains a specific string. This involves looping through each element of the array and comparing it to the specified string. If the element matches the string, then the loop returns `true`. Otherwise, it returns `false`.

**Section 3: Using the `Array.indexOf()` Method**

The `Array.indexOf()` method can be used to check if an array contains a specific string. This method returns the index of the first occurrence of the specified string in the array. If the string is not found in the array, then it returns `-1`.

**Section 4: Using the `Array.some()` Method**

The `Array.some()` method can also be used to check if an array contains a specific string. This method tests whether at least one element in the array passes the test implemented by the provided function. If the specified string is found in the array, then the function returns `true`. Otherwise, it returns `false`.
