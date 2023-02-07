---
title: What is the correct way to use jquery.inarray()?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: jQuery.inArray() is used to search for a specified value within an array and return its index (or -1 if not found).
---

**Contents**

[TOC]

# Introduction
jQuery.inArray() is a method used to search for an element within an array and return its position. It is a part of the jQuery library and is used to find the index of an element within an array.

# Syntax
The syntax for jQuery.inArray() is as follows:

```
jQuery.inArray(value, array[, fromIndex])
```

- `value`: The value to search for.
- `array`: An array through which to search.
- `fromIndex` (optional): The index at which to begin the search.

# Example
The following example demonstrates how to use jQuery.inArray():

```
var array = [1, 2, 3, 4, 5];

var index = jQuery.inArray(3, array);

console.log(index); // Outputs 2
```

In the example above, we search for the value `3` in the array `[1, 2, 3, 4, 5]` and the output is `2`, which is the index of the value `3` in the array.

# Conclusion
jQuery.inArray() is a useful method for finding the index of an element within an array. It is easy to use and can be used to quickly search through an array.
