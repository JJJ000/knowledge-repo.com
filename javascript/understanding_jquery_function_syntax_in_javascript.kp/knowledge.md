---
title: What does the code snippet (function($) {})(jquery); do?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-08 00:00:00
updated_at: 2023-02-08 00:00:00
tldr: This is an Immediately Invoked Function Expression (IIFE) which takes jQuery as an argument and runs the code inside the function.
---

**Contents**

[TOC]

# Overview
(function($) {})(jQuery); is a self-invoking anonymous function in Javascript. This type of function is often used to encapsulate code within a scope and to prevent any variables from leaking into the global scope.

# Syntax
The syntax for a self-invoking anonymous function is as follows:

(function(parameters) {
    // code to be executed
})(arguments);

In this example, the parameters are "$" and the argument is "jQuery".

# Benefits
The benefits of using a self-invoking anonymous function are:

- It keeps variables from leaking into the global scope, which can cause unintended consequences.
- It helps to keep code organized by encapsulating it within a scope.
- It allows for code to be executed immediately, without needing to be called explicitly.

# Conclusion
Self-invoking anonymous functions are a useful tool for encapsulating code and preventing unintended consequences. They can be used to keep code organized and allow for code to be executed immediately.
