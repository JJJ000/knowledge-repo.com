---
title: The difference between 'var functionname = function() {}' and 'function functionname() {}' is that the former assigns the function to a variable, while the latter declares the function directly
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-01-27 00:00:00
updated_at: 2023-01-27 00:00:00
tldr: The only difference between the two is that `functionName = function() {}` assigns the function to a variable, while `function functionName() {}` defines the function without assigning it to a variable.
---

**Contents**

[TOC]

### Syntax
The syntax for declaring a function in Javascript is `function functionName() { ... }`. The syntax for declaring a function expression is `var functionName = function() { ... }`.

### Scope
Function declarations are hoisted to the top of the containing scope, meaning that they can be called before they are declared in the code. Function expressions are not hoisted and can only be called after they are declared.

### Usage
Function declarations are generally used when a function needs to be called from multiple places in the code. Function expressions are generally used when a function needs to be passed as an argument to another function or when the function needs to be created conditionally.

### Performance
Function declarations are slightly faster than function expressions since they are hoisted. However, the difference in performance is so small that it should not be a factor in deciding which syntax to use.
