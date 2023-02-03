---
title: What is the syntax for passing a parameter to a settimeout() callback?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-03 00:00:00
updated_at: 2023-02-03 00:00:00
tldr: Pass the parameter(s) as additional argument(s) to the setTimeout() function.
---

**Contents**

[TOC]

### Set Up the SetTimeout Function

The setTimeout() function is a method of the window object that allows you to execute a function after a specified amount of time has passed. It takes two parameters: a callback function and a delay (in milliseconds).

```javascript
setTimeout(function() {
    // code to execute after delay
}, delay);
```

### Pass the Parameter

You can pass a parameter to the callback function by wrapping it in an anonymous function and passing the parameter to that anonymous function.

```javascript
let parameter = 'value';

setTimeout(function() {
    // code to execute after delay
    // parameter is available to use here
}, delay);
```

### Pass Multiple Parameters

If you need to pass multiple parameters to the callback function, you can wrap the callback function in an anonymous function and pass the parameters to that anonymous function.

```javascript
let parameter1 = 'value1';
let parameter2 = 'value2';

setTimeout(function() {
    // code to execute after delay
    // parameters are available to use here
}, delay);
```

### Use ES6 Arrow Function

If you're using an ES6 compatible browser, you can also use an arrow function to pass the parameters.

```javascript
let parameter = 'value';

setTimeout(() => {
    // code to execute after delay
    // parameter is available to use here
}, delay);
```
