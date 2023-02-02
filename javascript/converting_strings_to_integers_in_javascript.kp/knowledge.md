---
title: What is the process for changing a string to an integer in javascript?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-02 00:00:00
updated_at: 2023-02-02 00:00:00
tldr: Use the built-in parseInt() function to convert a string to an integer in JavaScript.
---

**Contents**

[TOC]

# Section 1: Using parseInt()
The `parseInt()` function is a built-in JavaScript function that is used to convert a string to an integer. It takes two parameters: the string to be converted, and an optional radix (base) which is used to specify the base of the number in the string.

# Section 2: Syntax
The syntax for using `parseInt()` is as follows:

```javascript
parseInt(string, radix);
```

# Section 3: Examples
Here are some examples of using `parseInt()`:

```javascript
// Convert a string to an integer with a base of 10
let str = "10";
let num = parseInt(str, 10);
console.log(num); // Output: 10

// Convert a string to an integer with a base of 16
let str = "FF";
let num = parseInt(str, 16);
console.log(num); // Output: 255
```

# Section 4: Caveats
It is important to note that `parseInt()` will only work on strings that contain only numerical characters. If the string contains any non-numerical characters, it will return `NaN` (Not a Number).
