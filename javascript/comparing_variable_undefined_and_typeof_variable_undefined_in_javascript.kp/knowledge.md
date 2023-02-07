---
title: Variable is undefined" versus "the type of variable is "undefined
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: The difference between `undefined` and `typeof variable === `undefined`` is that the former checks if a variable is undefined, whereas the latter checks the data type of a variable and returns `undefined` if it is undefined.
---

**Contents**

[TOC]

# Difference
The difference between `variable === undefined` and `typeof variable === "undefined"` is that the first statement checks if the value of the variable is undefined, whereas the second statement checks if the type of the variable is undefined.

# Examples

For example, if we have a variable `var x = undefined`, then `x === undefined` would evaluate to `true`, but `typeof x === "undefined"` would evaluate to `false`.

On the other hand, if we have a variable `var x;`, then `x === undefined` would evaluate to `true`, and `typeof x === "undefined"` would also evaluate to `true`.

# Usage
It is generally recommended to use `typeof variable === "undefined"` instead of `variable === undefined`, as it provides more accurate results.
