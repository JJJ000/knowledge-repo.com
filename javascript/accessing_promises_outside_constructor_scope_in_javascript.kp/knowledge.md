---
title: Solve a JavaScript promise that was created outside of the promise constructor
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Promises can be resolved by calling the resolve() or reject() methods on the Promise object.
---

**Contents**

[TOC]

### Solution 1:
Using `Promise.resolve()`

The `Promise.resolve()` method is used to create a new promise that is already resolved with the given value.

Syntax:
```js
Promise.resolve(value)
```

Example:
```js
let promise = Promise.resolve('Foo');

promise.then(value => console.log(value));
// expected output: "Foo"
```

### Solution 2:
Using `new Promise()`

The `new Promise()` constructor is used to create a new promise that can be resolved or rejected.

Syntax:
```js
new Promise((resolve, reject) => {
  // code
})
```

Example:
```js
let promise = new Promise((resolve, reject) => {
  resolve('Foo');
});

promise.then(value => console.log(value));
// expected output: "Foo"
```
