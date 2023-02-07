---
title: How does returning a value differ from using promise.resolve() within the then() function?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: Returning a value from then() will pass the value to the next then() in the chain, while Promise.resolve will resolve the promise and pass the value to the next then() in the chain.
---

**Contents**

[TOC]

1. **Returning Value**
When returning a value from the `then()` method, the value will be passed to the next chained `then()` method in the promise chain. This value can be of any type (e.g. string, number, object, array, etc.).

2. **Promise.resolve**
When using `Promise.resolve()` in the `then()` method, the resulting value will be wrapped in a new promise object. This new promise will then be passed to the next chained `then()` method in the promise chain. The value that is passed to `Promise.resolve()` can be of any type (e.g. string, number, object, array, etc.).
