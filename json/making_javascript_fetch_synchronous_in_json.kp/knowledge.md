---
title: What steps are necessary to make a JavaScript fetch operation run synchronously?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-12 00:00:00
updated_at: 2023-02-12 00:00:00
tldr: JavaScript fetch cannot be made synchronous, but can be made to appear synchronous using the async/await syntax.
---

**Contents**

[TOC]

1. Using `async/await`
  
  JavaScript `fetch` is asynchronous by default, so to make it synchronous, the `async/await` keywords can be used. `async/await` allows functions to be written synchronously, while still allowing them to be asynchronous.

2. Using `Promise.all()`
  
  `Promise.all()` is another way to make JavaScript `fetch` synchronous. `Promise.all()` takes an array of promises and returns a single promise that resolves when all of the promises in the array have been resolved.

3. Using `.then()`
  
  The `.then()` method can also be used to make JavaScript `fetch` synchronous. `.then()` takes a callback function that is executed when the promise it is chained to is resolved. The callback function is executed synchronously, so it can be used to make JavaScript `fetch` synchronous.

4. Using `.done()`
  
  The `.done()` method is similar to the `.then()` method, but it is used when the promise is already resolved. The `.done()` method takes a callback function that is executed when the promise is resolved. The callback function is executed synchronously, so it can be used to make JavaScript `fetch` synchronous.
