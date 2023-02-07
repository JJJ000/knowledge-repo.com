---
title: Is the array.foreach function in JavaScript and Node.js asynchronous?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: No, Array.forEach is synchronous in JavaScript.
---

**Contents**

[TOC]

# Synchronous vs Asynchronous

Synchronous code is code that is executed line-by-line in the order it is written. Asynchronous code is code that can be executed out of order, or in parallel.

# Array.forEach

Array.forEach is a method in JavaScript that allows you to iterate over an array and perform an action on each element. It is a synchronous function, meaning it will execute the code line-by-line in the order it is written.

# Node.js

In Node.js, Array.forEach is still a synchronous function. However, Node.js also has an asynchronous version of the function, which is called Array.forEachAsync. This version of the function allows you to execute code in parallel, and can be more efficient than the synchronous version.

# Conclusion

In conclusion, Array.forEach is a synchronous function in both JavaScript and Node.js. However, Node.js also has an asynchronous version of the function, Array.forEachAsync, which can be used to execute code in parallel.
