---
title: Do 'arrow functions' and 'functions' have the same purpose?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-03 00:00:00
updated_at: 2023-02-03 00:00:00
tldr: No, Arrow Functions are a more concise syntax for writing functions in JavaScript, but are not interchangeable with traditional functions.
---

**Contents**

[TOC]

##No

Although arrow functions and functions are both used to create functions in JavaScript, they are not equivalent or interchangeable. 

##Arrow Functions

Arrow functions are a new syntax for writing JavaScript functions. They are shorter than traditional function expressions and are always anonymous. Arrow functions are best suited for non-method functions, and they do not have their own this, arguments, super, or new.target. 

##Functions

Functions are a set of statements that perform a task or calculate a value. They are defined with the function keyword, followed by a name, a list of parameters, and a body. The body is a collection of statements that specifies what the function does. Functions can be used to define methods to objects, and they can be called from other functions or code. Functions can also have their own this, arguments, super, and new.target. 

##Conclusion

In conclusion, arrow functions and functions are not equivalent or interchangeable in JavaScript. Arrow functions are best suited for non-method functions and do not have their own this, arguments, super, or new.target. On the other hand, functions are a set of statements that can be used to define methods to objects, and they can have their own this, arguments, super, and new.target.
