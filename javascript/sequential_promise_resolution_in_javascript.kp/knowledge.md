---
title: Fulfill promises in order
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: Promises can be chained together using the `.then()` method to execute them in sequence.
---

**Contents**

[TOC]

# Section 1: Using `Promise.all()`

The `Promise.all()` method allows you to execute a set of promises in sequence. It takes an array of promises as an argument and returns a single promise that resolves when all of the promises in the array have been resolved. The returned promise resolves with an array of the resolved values of each promise in the order they were passed in.

# Section 2: Using `async/await`

The `async/await` syntax provides an easy way to execute promises in sequence. An `async` function returns a promise, and `await` can be used to wait for a promise to resolve before continuing. This allows you to write code that looks synchronous, but is actually asynchronous.

# Section 3: Using `.then()`

The `.then()` method can be used to chain promises together in sequence. This allows you to create a sequence of promises that will be executed one after the other. The `.then()` method returns a new promise that resolves with the value returned by the previous promise.

# Section 4: Using Recursion

Recursion can be used to execute promises in sequence. This involves creating a function that calls itself, passing in the next promise in the sequence. This allows you to execute promises one after the other until all of the promises have been resolved.
