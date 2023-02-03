---
title: What is the syntax for setting the size of an array in javascript?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-03 00:00:00
updated_at: 2023-02-03 00:00:00
tldr: The length of an array in JavaScript can be initialized by assigning a numerical value to the array`s length property.
---

**Contents**

[TOC]

1. Declaring an Array 

In JavaScript, an array can be declared using the `var` keyword followed by the array name and square brackets `[]`. For example, to declare an array named `myArray`, the syntax would be: 

```
var myArray = [];
```

2. Initializing an Array 

An array can be initialized with values by adding the values inside the square brackets `[]` separated by commas. For example, to initialize `myArray` with the values `1`, `2`, and `3`, the syntax would be: 

```
var myArray = [1, 2, 3];
```

3. Setting the Array Length 

The `length` property of an array can be used to set the length of the array. This can be done by assigning a numerical value to the `length` property. For example, to set `myArray` to a length of `5`, the syntax would be: 

```
myArray.length = 5;
```

4. Result

After setting the `length` property, the array will be padded with `undefined` values to match the new length. In the example above, `myArray` will be set to `[1, 2, 3, undefined, undefined]`.
