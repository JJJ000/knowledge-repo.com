---
title: What is the correct method for waiting until a function has completed before proceeding?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: The proper way to wait for one function to finish before continuing in Javascript is to use a callback function.
---

**Contents**

[TOC]

1. Using Callbacks 

Callbacks are functions that are passed as an argument to another function and are executed after the outer function has finished executing. Callbacks are a great way to ensure that one function has finished executing before continuing on with the rest of the code.

2. Using Promises 

Promises are objects that represent the eventual completion or failure of an asynchronous operation. They provide a way to ensure that one function has finished executing before continuing on with the rest of the code.

3. Using Async/Await 

Async/Await is a language feature that allows you to write asynchronous code in a synchronous style. It provides a way to ensure that one function has finished executing before continuing on with the rest of the code.

4. Using Event Listeners 

Event Listeners are functions that are triggered when a certain event is fired. They provide a way to ensure that one function has finished executing before continuing on with the rest of the code.
