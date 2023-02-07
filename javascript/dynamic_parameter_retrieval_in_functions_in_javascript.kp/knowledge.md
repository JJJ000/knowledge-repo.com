---
title: What is the process for obtaining the names and values of function parameters dynamically?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: You can use the arguments object to access the parameter names and values of a function dynamically in Javascript.
---

**Contents**

[TOC]

#### Using `arguments` Object

The `arguments` object is a local variable available within all non-arrow functions. It contains an entry for each argument passed to the function, with the first entry's index at 0.

For example, given the following function:

```js
function add(a, b) {
  return a + b;
}
```

We can access the parameters `a` and `b` using the `arguments` object:

```js
function add(a, b) {
  console.log(arguments[0]); // a
  console.log(arguments[1]); // b
  return a + b;
}
```

#### Using `Object.keys()`

The `Object.keys()` method can be used to get the list of parameter names for a given function. It takes an object as an argument and returns an array of strings that represent the object's keys.

Given the following function:

```js
function add(a, b) {
  return a + b;
}
```

We can use `Object.keys()` to get an array of the parameter names:

```js
const params = Object.keys(add); // ['a', 'b']
```

#### Using `Object.getOwnPropertyNames()`

The `Object.getOwnPropertyNames()` method can be used to get the list of parameter names and values for a given function. It takes an object as an argument and returns an array of strings that represent the object's own property names.

Given the following function:

```js
function add(a, b) {
  return a + b;
}
```

We can use `Object.getOwnPropertyNames()` to get an array of the parameter names and values:

```js
const params = Object.getOwnPropertyNames(add); // ['a', 'b', 'length', 'name', 'prototype']
```

#### Using `Function.prototype.toString()`

The `Function.prototype.toString()` method can be used to get the source code of a given function. It returns a string containing the source code of the function.

Given the following function:

```js
function add(a, b) {
  return a + b;
}
```

We can use `Function.prototype.toString()` to get the source code of the function:

```js
const source = add.toString(); // 'function add(a, b) { return a + b; }'
```

From the source code, we can parse out the parameter names:

```js
const params = source.match(/\(([^)]+)\)/)[1].split(', '); // ['a', 'b']
```
