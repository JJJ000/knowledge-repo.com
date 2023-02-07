---
title: Eliminate duplicates from array using lodash
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: Lodash can be used to remove duplicates from an array in Javascript using the uniq() method.
---

**Contents**

[TOC]

# Section 1 - Overview

Lodash is a JavaScript library that provides utility functions for common programming tasks. It can be used to remove duplicates from an array of values. The _.uniq() method is used to remove duplicate values from an array.

# Section 2 - Syntax

The syntax for the _.uniq() method is as follows:

```
_.uniq(array)
```

# Section 3 - Parameters

The _.uniq() method takes an array as its only parameter.

# Section 4 - Examples

Here are some examples of using the _.uniq() method to remove duplicates from an array:

```
// Remove duplicate numbers from an array
let numbers = [1, 2, 3, 4, 5, 1, 2, 3];
let uniqueNumbers = _.uniq(numbers);
console.log(uniqueNumbers); // [1, 2, 3, 4, 5]

// Remove duplicate strings from an array
let strings = ["foo", "bar", "baz", "foo", "bar"];
let uniqueStrings = _.uniq(strings);
console.log(uniqueStrings); // ["foo", "bar", "baz"]
```
