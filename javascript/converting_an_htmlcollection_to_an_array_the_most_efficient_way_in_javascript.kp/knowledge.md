---
title: The quickest way to turn an htmlcollection into an array
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: The most efficient way to convert an HTMLCollection to an Array is to use the Array.from() method.
---

**Contents**

[TOC]

**Section 1: Using Array.from()**

The most efficient way to convert an HTMLCollection to an Array in Javascript is to use the Array.from() method. This method creates a new, shallow-copied Array instance from an array-like or iterable object. It takes the HTMLCollection as an argument and returns a new Array with the same elements.

**Section 2: Using the Spread Operator**

Another efficient way to convert an HTMLCollection to an Array in Javascript is to use the spread operator. The spread operator takes the HTMLCollection as an argument and returns a new Array with the same elements. This is a more concise way to accomplish the same task as using the Array.from() method.

**Section 3: Using the forEach() Method**

The forEach() method can also be used to convert an HTMLCollection to an Array in Javascript. This method iterates through each element in the HTMLCollection and adds them to a new Array. This is a more verbose approach than the previous two methods, but it is still efficient.

**Section 4: Using the Array.prototype.slice() Method**

The Array.prototype.slice() method can also be used to convert an HTMLCollection to an Array in Javascript. This method takes the HTMLCollection as an argument and returns a new Array with the same elements. This is a more efficient approach than using the forEach() method, but it is still more verbose than the first two methods.
