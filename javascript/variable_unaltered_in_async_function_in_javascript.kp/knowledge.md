---
title: Why hasn't my variable changed after I edited it inside a function, given that the code is asynchronous?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-03 00:00:00
updated_at: 2023-02-03 00:00:00
tldr: The variable is not modified because the function is running asynchronously and the changes may not have been applied before the code continues to run.
---

**Contents**

[TOC]

# Synchronous vs. Asynchronous Code
Synchronous code is code that is executed one line at a time and in the order it is written. This means that each line of code is executed in order and the next line of code is not executed until the current line of code has completed. Asynchronous code, on the other hand, is code that can be executed out of order and can be run at the same time as other code. This type of code is more complex and can be difficult to debug.

# Variable Scope
When working with variables inside of functions, it is important to understand the concept of variable scope. Variable scope defines where a variable is accessible and how it can be modified. In JavaScript, variables declared inside of a function are only accessible within the function and any changes made to the variable are not reflected in the global scope.

# Closures
A closure is a special type of function that allows a variable declared inside of a function to be accessible outside of the function. This allows the variable to be modified outside of the function and for the changes to be reflected in the global scope. Closures are often used to create variables that can be accessed and modified across multiple functions.

# Conclusion
When working with variables in JavaScript, it is important to understand the concept of variable scope, synchronous and asynchronous code, and closures. Understanding these concepts can help ensure that variables are accessible and can be modified outside of the function they are declared in.
