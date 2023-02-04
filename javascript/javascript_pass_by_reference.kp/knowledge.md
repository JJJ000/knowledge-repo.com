---
title: Is JavaScript a pass-by-reference language?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-04 00:00:00
updated_at: 2023-02-04 00:00:00
tldr: No, JavaScript passes by value.
---

**Contents**

[TOC]

## No

JavaScript passes by value, not by reference. When a variable is passed to a function, the value of the variable is copied to the function's internal scope. Any changes made to the variable within the function will not affect the original variable outside of the function.

## Explanation

When a variable is passed to a function, a copy of the variable’s value is created and stored in the function’s internal scope. This means that any changes made to the variable within the function will not affect the original variable outside of the function. This is known as passing by value.

In contrast, passing by reference involves passing a reference to the original variable to the function. This means that any changes made to the variable within the function will be reflected in the original variable outside of the function.

## Examples

Let's look at an example to better understand how JavaScript passes by value.

```javascript
let x = 10;

function addFive(num) {
  num += 5;
  return num;
}

let y = addFive(x);

console.log(x); // 10
console.log(y); // 15
```

In this example, `x` is passed to the `addFive()` function. A copy of `x`'s value is created and stored in the function's internal scope. The value is then incremented by 5 and returned.

The value of `x` outside of the function remains unchanged, while the value of `y` is set to the new value returned by the function. This demonstrates that JavaScript passes by value, not by reference.
