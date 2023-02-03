---
title: How can I call a JavaScript function when I have its name as a string?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-03 00:00:00
updated_at: 2023-02-03 00:00:00
tldr: You can use the JavaScript function eval() to execute a JavaScript function when you have its name as a string.
---

**Contents**

[TOC]

##### Using eval()

The `eval()` function can be used to execute a JavaScript function when its name is given as a string. It takes a string as an argument and evaluates it as if it were JavaScript code.

```
let funcName = 'myFunction';
let func = eval(funcName);
func(); // This will execute the function
```

##### Using Function Constructor

The `Function` constructor can also be used to execute a JavaScript function when its name is given as a string. It takes two arguments: a string of comma-separated argument names and a string containing the JavaScript code for the function body.

```
let funcName = 'myFunction';
let func = new Function(funcName);
func(); // This will execute the function
```

##### Using Function.prototype.call()

The `Function.prototype.call()` method can also be used to execute a JavaScript function when its name is given as a string. It takes one argument: the this value for the function.

```
let funcName = 'myFunction';
let func = window[funcName];
func.call(null); // This will execute the function
```
