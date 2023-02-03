---
title: What is the difference between javascript's call(), apply(), and bind() methods?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-03 00:00:00
updated_at: 2023-02-03 00:00:00
tldr: Call and Apply invoke the function immediately, whereas Bind returns a new function that can be invoked later.
---

**Contents**

[TOC]

### Call()

The `call()` method calls a function with a given this value and arguments provided individually.

### Syntax

```
fun.call(thisArg, arg1, arg2, ...)
```

### Apply()

The `apply()` method calls a function with a given this value, and arguments provided as an array (or an array-like object).

### Syntax

```
fun.apply(thisArg, [argsArray])
```

### Bind()

The `bind()` method creates a new function that, when called, has its this keyword set to the provided value, with a given sequence of arguments preceding any provided when the new function is called.

### Syntax

```
fun.bind(thisArg[, arg1[, arg2[, ...]]])
```
