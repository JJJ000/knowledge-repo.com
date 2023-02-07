---
title: How can named parameters be used when calling a function in javascript?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: No, there is no way to provide named parameters in a function call in JavaScript.
---

**Contents**

[TOC]

## No

Named parameters are not a feature of the JavaScript language.

## Alternatives

One alternative is to use an object literal to pass parameters to a function. This can be done by creating an object with the desired parameters, and passing the object as an argument to the function.

```javascript
function foo(options) {
  console.log(options.param1);
  console.log(options.param2);
}

let params = {
  param1: 'value1',
  param2: 'value2'
};

foo(params);
```

Another alternative is to use the ES6 spread operator to spread the parameters of an array into the arguments of a function.

```javascript
function foo(param1, param2) {
  console.log(param1);
  console.log(param2);
}

let params = ['value1', 'value2'];

foo(...params);
```
