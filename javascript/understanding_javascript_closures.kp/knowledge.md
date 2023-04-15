---
title: What is the functioning of JavaScript closures?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-04-17 00:00:00
updated_at: 2023-04-17 00:00:00
tldr: A closure is an inner function that has access to the variables in the outer (enclosing) function`s scope chain.
---

**Contents**

[TOC]

### Definition
A closure is an inner function that has access to the outer (enclosing) function’s variables—scope chain. The closure has three scope chains: it has access to its own scope (variables defined between its curly brackets), it has access to the outer function’s variables, and it has access to the global variables.

### Benefits
Closures are useful because they let you associate some data (the lexical environment) with a function that operates on that data. This has obvious parallels to object oriented programming, where objects allow us to associate some data (the object's properties) with one or more methods.

### Example
An example of a closure is shown below:

```javascript
function outerFunction(x) {
  let innerVariable = 3;

  function innerFunction(y) {
    return x + y + innerVariable;
  }

  return innerFunction;
}

let myClosure = outerFunction(1);
myClosure(2); // 6
```

### Usage
Closures are often used in JavaScript for object data privacy, partial application, and currying. Additionally, they can be used to create closures that will persist after the outer function has returned, which is useful for asynchronous programming.
