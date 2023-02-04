---
title: Are promises essentially the same as callbacks?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-04 00:00:00
updated_at: 2023-02-04 00:00:00
tldr: No, promises are not just callbacks, but rather a more structured way of handling asynchronous operations.
---

**Contents**

[TOC]

###No
Promises are not just callbacks in Javascript. While they are both asynchronous programming techniques, promises and callbacks have different purposes and implementations.

###Callbacks
Callbacks are functions that are passed as an argument to another function. The function that is passed as an argument is then executed after certain conditions are met. Callbacks are commonly used for asynchronous programming, especially in Node.js.

###Promises
Promises are objects that represent the eventual completion or failure of an asynchronous operation. They provide a way to handle asynchronous operations in a more synchronous way, by allowing the user to write code that looks like synchronous code. Promises also have a set of methods that allow the user to handle errors and results.
