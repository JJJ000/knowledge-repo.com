---
title: Change a string into a variable name in javascript
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-08 00:00:00
updated_at: 2023-02-08 00:00:00
tldr: The string can be converted to a variable name using the `eval()` function.
---

**Contents**

[TOC]

**Section 1: Using the eval() Function**

The `eval()` function can be used to convert a string to a variable name. This is done by passing the string as an argument in the `eval()` function.

For example:

```js
let str = 'foo';
let foo = 'bar';

let x = eval(str);
console.log(x); // Outputs 'bar'
```

**Section 2: Using the window Object**

The `window` object can also be used to convert a string to a variable name. This is done by using the `window` object to access the variable by passing the string as a key.

For example:

```js
let str = 'foo';
let foo = 'bar';

let x = window[str];
console.log(x); // Outputs 'bar'
```

**Section 3: Using the Function Constructor**

The `Function` constructor can be used to convert a string to a variable name. This is done by passing the string as an argument in the `Function` constructor.

For example:

```js
let str = 'foo';
let foo = 'bar';

let x = new Function('return ' + str)();
console.log(x); // Outputs 'bar'
```

**Section 4: Using the Object Constructor**

The `Object` constructor can also be used to convert a string to a variable name. This is done by passing the string as an argument in the `Object` constructor.

For example:

```js
let str = 'foo';
let foo = 'bar';

let x = new Object(str);
console.log(x); // Outputs 'bar'
```
