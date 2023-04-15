---
title: What is the equivalent of sleep() in javascript?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-04-17 00:00:00
updated_at: 2023-04-17 00:00:00
tldr: There is no direct equivalent of the sleep() function in JavaScript; however, setTimeout() can be used to delay code execution.
---

**Contents**

[TOC]

**setTimeout()**

The setTimeout() method is the JavaScript version of sleep(). It is a function that can be used to delay the execution of a certain code until a certain amount of time has passed.

**Syntax**

The syntax for the setTimeout() method is as follows:

setTimeout(function, milliseconds);

The first argument is a function that will be executed after the specified number of milliseconds. The second argument is the number of milliseconds that must pass before the function is executed.

**Example**

For example, the following code will execute the function "myFunction" after 1000 milliseconds (1 second):

setTimeout(myFunction, 1000);

**Conclusion**

In conclusion, the setTimeout() method is the JavaScript version of sleep(). It is a function that can be used to delay the execution of a certain code until a certain amount of time has passed.
