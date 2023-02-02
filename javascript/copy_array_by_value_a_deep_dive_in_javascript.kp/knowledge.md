---
title: Duplicate the contents of an array
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-02 00:00:00
updated_at: 2023-02-02 00:00:00
tldr: To copy an array by value in Javascript, use the Array.prototype.slice() method.
---

**Contents**

[TOC]

1. **Using the Spread Operator**
   The spread operator (`...`) can be used to create a shallow copy of an array. The spread operator expands an array into its individual elements.

2. **Using the Array.from() Method**
   The `Array.from()` method can also be used to create a shallow copy of an array. This method takes two arguments: an array-like object or an iterable object.

3. **Using the Array.slice() Method**
   The `Array.slice()` method can be used to create a shallow copy of an array. The `slice()` method takes two arguments: the start index and the end index.

4. **Using the Array.concat() Method**
   The `Array.concat()` method can also be used to create a shallow copy of an array. This method takes one or more arrays as arguments and returns a new array with the elements of all the arrays combined.
