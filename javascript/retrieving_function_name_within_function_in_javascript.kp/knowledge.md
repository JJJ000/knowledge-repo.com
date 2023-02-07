---
title: What is the name of the function I am currently in?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: You can use the `arguments.callee.name` property to get the function name from within the function in Javascript.
---

**Contents**

[TOC]

### Using `arguments.callee`

The `arguments.callee` property is a reference to the currently executing function. It can be used to retrieve the function name from within the function body.

```javascript
function myFunction() {
  console.log(arguments.callee.name);
  // Outputs: "myFunction"
}
```

### Using `Function.prototype.name`

The `Function.prototype.name` property returns the name of the function. This is supported in all modern browsers, with the exception of Internet Explorer.

```javascript
function myFunction() {
  console.log(myFunction.name);
  // Outputs: "myFunction"
}
```

### Using `Function.prototype.toString()`

The `Function.prototype.toString()` method returns a string representation of the function. This can be used to extract the function name.

```javascript
function myFunction() {
  const funcString = myFunction.toString();
  const funcName = funcString.substring(funcString.indexOf(' ') + 1, funcString.indexOf('('));
  console.log(funcName);
  // Outputs: "myFunction"
}
```

### Using `console.trace()`

The `console.trace()` method prints a stack trace to the console, which can be used to extract the function name.

```javascript
function myFunction() {
  console.trace();
  // Outputs: 
  // myFunction
  //     at <anonymous>:2:13
  //     at <anonymous>:4:3
  //     at <anonymous>:1:1
  const funcString = console.trace()[0];
  const funcName = funcString.substring(funcString.indexOf(' ') + 1, funcString.indexOf('('));
  console.log(funcName);
  // Outputs: "myFunction"
}
```
