---
title: Comparing JavaScript closures and anonymous functions
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: A closure is a function that remembers and accesses its lexical scope even when that function is executing outside its lexical scope, whereas an anonymous function is a function that does not have a name.
---

**Contents**

[TOC]

### JavaScript Closures

A JavaScript closure is a function defined inside another function (the parent function) and has access to variables declared and defined in the parent function’s scope. The closure has access to the parent function’s variables, and any other variables declared in the global scope. The closure will keep these variables alive even after the parent function has returned.

### Anonymous Functions

An anonymous function is a function that has no name. It is usually defined and passed as an argument to another function, or assigned to a variable. Anonymous functions are often used in JavaScript to create callback functions. They are also commonly used in jQuery to define event handlers.

### Differences

The main difference between a closure and an anonymous function is that a closure has access to variables in the parent function’s scope, while an anonymous function does not. Additionally, a closure can be used to preserve state, while an anonymous function cannot. Finally, a closure can be used to create a private scope, while an anonymous function cannot.
