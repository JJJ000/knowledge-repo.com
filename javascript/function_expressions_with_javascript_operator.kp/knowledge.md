---
title: Adding a plus sign before a JavaScript function expression
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-03 00:00:00
updated_at: 2023-02-03 00:00:00
tldr: A plus sign in front of a function expression in Javascript indicates that the function should be treated as a number.
---

**Contents**

[TOC]

# Syntax
The syntax for a function expression in JavaScript with a plus sign in front of it is:

`+function() {
  // Function body
}`

# Purpose
The plus sign in front of a function expression is used to indicate that the function should be executed immediately. This is known as an Immediately Invoked Function Expression (IIFE). 

# Benefits
IIFEs have several benefits. They create a new scope, which helps to prevent variables from leaking into the global scope. Additionally, they can be used to create closures and to execute code immediately, which can be useful when writing asynchronous code.

# Example
For example, the following code creates an IIFE that logs the message "Hello World":

`+function() {
  console.log('Hello World');
}();`
