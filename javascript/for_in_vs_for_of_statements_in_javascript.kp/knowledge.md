---
title: What is the distinction between a 'for... in' loop and a 'for... of' loop?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-03 00:00:00
updated_at: 2023-02-03 00:00:00
tldr: The for...in statement iterates over the properties of an object, while the for...of statement iterates over the values of an iterable object.
---

**Contents**

[TOC]

# for... in
The `for...in` statement is used to iterate over the enumerable properties of an object. It works by looping through each property of an object and executing a block of code for each property.

# for... of
The `for...of` statement is used to iterate over the iterable objects such as arrays, strings, maps, sets, and arguments objects. It works by looping through each element of an iterable object and executing a block of code for each element. 

# Difference
The main difference between `for...in` and `for...of` statements is that `for...in` iterates over the properties of an object, while `for...of` iterates over the elements of an iterable object. In addition, `for...in` loops through all enumerable properties, including those inherited through the prototype chain, while `for...of` only iterates over own properties of the object.
