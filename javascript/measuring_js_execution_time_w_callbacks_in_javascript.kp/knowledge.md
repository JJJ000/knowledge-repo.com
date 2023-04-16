---
title: What is the most effective way to determine the amount of time it takes for JavaScript code with callbacks to be executed?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: You can measure the execution time of JavaScript code with callbacks by using the Date.now() function.
---

**Contents**

[TOC]

## Using console.time()
The `console.time()` function can be used to measure the execution time of JavaScript code. It takes a label as an argument and stores the start time. After the code has finished executing, `console.timeEnd()` is called with the same label, and the elapsed time is printed in the console.

For example:

```javascript
console.time('execution time');

// Code with callbacks

console.timeEnd('execution time');
```

## Using performance.now()
The `performance.now()` function can be used to measure the execution time of JavaScript code. This function returns the elapsed time in milliseconds since the page was loaded.

For example:

```javascript
let startTime = performance.now();

// Code with callbacks

let endTime = performance.now();
let elapsedTime = endTime - startTime;
console.log(elapsedTime);
```

## Using Date.now()
The `Date.now()` function can also be used to measure the execution time of JavaScript code. This function returns the elapsed time in milliseconds since the Unix epoch.

For example:

```javascript
let startTime = Date.now();

// Code with callbacks

let endTime = Date.now();
let elapsedTime = endTime - startTime;
console.log(elapsedTime);
```
