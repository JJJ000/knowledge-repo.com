---
title: What is the best way to reference the correct 'this' within a callback function?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Use `.bind()` to explicitly set the value of `this` inside the callback.
---

**Contents**

[TOC]

### Use Arrow Functions

Arrow functions are a great way to access the correct `this` inside a callback in Javascript. Arrow functions do not have their own `this`, so they use the `this` of the enclosing scope. This means that the `this` used inside the arrow function is the same `this` as outside the arrow function.

### Use `.bind()`

Another way to access the correct `this` inside a callback in Javascript is to use the `.bind()` method. This method allows you to explicitly set the `this` value to the object you want.

### Use `.call()`

The `.call()` method can also be used to access the correct `this` inside a callback in Javascript. The `.call()` method allows you to explicitly set the `this` value to the object you want, just like the `.bind()` method.

### Use `.apply()`

The `.apply()` method is similar to the `.call()` method, but it takes an array of arguments instead of a list of arguments. This can be useful if you need to pass in a variable number of arguments to the callback.
