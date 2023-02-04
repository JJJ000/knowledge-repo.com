---
title: What is the most effective way to turn the "arguments" object into an array in javascript?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-04 00:00:00
updated_at: 2023-02-04 00:00:00
tldr: You can convert the `arguments` object to an array in JavaScript using the Array.from() method.
---

**Contents**

[TOC]

# Section 1: Using Array.from()
The `Array.from()` method can be used to convert the `arguments` object to an array.

# Section 2: Syntax
The syntax for using the `Array.from()` method is as follows:

```
Array.from(arguments)
```

# Section 3: Example
The following example shows how to use the `Array.from()` method to convert the `arguments` object to an array:

```
function myFunc() {
  let args = Array.from(arguments);
  console.log(args);
}

myFunc(1, 2, 3); // [1, 2, 3]
```

# Section 4: Browser Support
The `Array.from()` method is supported in all modern browsers, including Chrome, Firefox, Edge, and Safari.
