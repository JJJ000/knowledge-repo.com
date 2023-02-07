---
title: Is it possible to assign variables to undefined or provide undefined as an argument?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: Yes, you can set variables to undefined or pass undefined as an argument in Javascript.
---

**Contents**

[TOC]

Yes, you can set variables to undefined or pass undefined as an argument in Javascript.

## Setting Variables to Undefined

You can set a variable to undefined in Javascript by simply assigning it the value `undefined`.

```js
let myVar;
// myVar is now undefined
```

## Passing Undefined as an Argument

You can also pass undefined as an argument to a function. This is useful when you want to indicate that an argument is optional.

```js
function myFunc(myArg = undefined) {
  // Do something with myArg
}
```

## Checking for Undefined

When working with undefined values, it is important to be aware of the difference between `undefined` and `null`. `undefined` indicates that a variable has been declared but not assigned a value, while `null` indicates that a variable has been assigned a value of `null`.

You can use the `typeof` operator to check if a variable is `undefined`:

```js
let myVar;

if (typeof myVar === 'undefined') {
  console.log('myVar is undefined');
}
```
