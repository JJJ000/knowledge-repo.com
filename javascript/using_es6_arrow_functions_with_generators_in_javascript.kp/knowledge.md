---
title: Is it possible to use the arrow function syntax of es6 with generators (in the arrow notation)?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: Yes, arrow functions can be used with generators in JavaScript.
---

**Contents**

[TOC]

**Yes**

**Using Arrow Notation with Generators**

Generators are a type of function that allow for the creation of iterators. They are written using the function* syntax and the yield keyword. Arrow functions can be used with generators in order to simplify the syntax and make code more concise.

**Syntax**

The syntax for using arrow functions with generators is similar to the syntax for regular arrow functions. The only difference is that the function keyword is replaced with the function* keyword. The following example shows the syntax for an arrow function generator:

```
const generator = () => {
  yield* [1, 2, 3];
};
```

**Benefits**

Using arrow functions with generators can help to make code more concise and readable. It also allows for the creation of more complex iterators with less code. Additionally, arrow functions can be used to create recursive generators, which can be used to create more efficient algorithms.
