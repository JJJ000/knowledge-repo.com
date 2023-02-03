---
title: What does the (function() { } )() syntax do in javascript?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-03 00:00:00
updated_at: 2023-02-03 00:00:00
tldr: The (function() { } )() construct is an Immediately Invoked Function Expression (IIFE) which allows a function to be executed as soon as it is defined.
---

**Contents**

[TOC]

# Overview
The (function() { } )() construct in JavaScript is an Immediately Invoked Function Expression (IIFE) that creates a new scope and executes the code within it. It is often used to keep variables and functions out of the global scope, and to provide privacy and encapsulation for the code.

# Syntax
The syntax for an IIFE is as follows:

(function() {
    // code here
})();

# Benefits
The most common benefit of using an IIFE is that it keeps variables and functions out of the global scope. This helps to avoid namespace collisions and helps to make the code more organized and easier to maintain. It also provides privacy and encapsulation for the code, as the variables and functions defined within the IIFE are not accessible from the outside.

# Examples
The following example creates a variable within an IIFE and then logs the variable to the console:

(function() {
    let myVariable = 'Hello World!';
    console.log(myVariable);
})();

In this example, the variable myVariable is not accessible from outside of the IIFE.
