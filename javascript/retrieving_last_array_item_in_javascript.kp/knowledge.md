---
title: Retrieve the final element in an array
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-02 00:00:00
updated_at: 2023-02-02 00:00:00
tldr: The last item in an array in Javascript can be accessed using the array`s length property minus one, i.e. array[array.length - 1].
---

**Contents**

[TOC]

## Array Method

The `.pop()` method can be used to access the last item in an array. This method removes the last element from an array and returns that element. 

## Syntax

The syntax for the `.pop()` method is as follows:

```
array.pop()
```

## Example

The following example shows how to use the `.pop()` method to get the last item in an array:

```
let arr = [1, 2, 3, 4, 5];
let lastItem = arr.pop();
console.log(lastItem); // Output: 5
```

## Output

The output of the above code is `5`, which is the last item in the array.
