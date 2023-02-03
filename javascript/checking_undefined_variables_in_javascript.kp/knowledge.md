---
title: How to determine if a variable has been declared in javascript
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-03 00:00:00
updated_at: 2023-02-03 00:00:00
tldr: You can check if a variable is undefined by using the `typeof` operator.
---

**Contents**

[TOC]

1. Using typeof Operator
The typeof operator is used to check the data type of a not-defined variable in JavaScript. It returns undefined if the variable is not defined.

Syntax:

typeof variable_name

Example:

let x;
console.log(typeof x); // Output: undefined

2. Using Undefined Property
The undefined property is another way to check the not-defined variable in JavaScript. It returns true if the variable is not defined.

Syntax:

variable_name === undefined

Example:

let y;
console.log(y === undefined); // Output: true
