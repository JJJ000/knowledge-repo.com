---
title: Using an asynchronous function with the 'await' keyword and 'settimeout' to delay its execution
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Async function + await can be used to wait for a setTimeout to finish before executing the next line of code.
---

**Contents**

[TOC]

**Section 1 - Async Function** 

An async function is a special type of function that can contain asynchronous code. Async functions use the keyword `async` before the function definition, and the keyword `await` within the function body to pause the execution of the function until a Promise resolves.

**Section 2 - Await**

The `await` keyword is used to pause the execution of an async function until a Promise resolves. It can only be used within an async function and can only be used with Promises.

**Section 3 - SetTimeout**

The `setTimeout()` method is used to execute a function after a specified amount of time. It takes two arguments: a callback function, and a time in milliseconds.

**Section 4 - Combination**

The combination of async functions, await, and setTimeout can be used to execute asynchronous code in a controlled manner. For example, an async function could use `setTimeout()` to delay the execution of a Promise, then `await` the Promise to pause the function until the Promise resolves.
