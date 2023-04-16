---
title: How do function expressions and declarations differ in javascript?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: A function expression is a function that is assigned to a variable, while a function declaration is a function that is declared directly in the code.
---

**Contents**

[TOC]

### Function Declaration
A function declaration is a statement that declares a function and its name. This type of function is hoisted, meaning that the function can be called before it is declared.

### Function Expression
A function expression is a statement that assigns a function to a variable. This type of function is not hoisted, meaning that the function cannot be called before it is declared. 

### Syntax
Function declarations use the `function` keyword followed by the name of the function. Function expressions use a variable name followed by the `function` keyword.

### Example

Function Declaration:
```
function sayHello() {
  console.log('Hello World!');
}
```

Function Expression:
```
const sayHello = function() {
  console.log('Hello World!');
}
```
