---
title: What is the duration of a function's execution?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: You can measure the time taken by a function to execute in Javascript by using the performance.now() method.
---

**Contents**

[TOC]

## Using `performance.now()`

The `performance.now()` method returns a DOMHighResTimeStamp, measured in milliseconds, accurate to one thousandth of a millisecond.

To measure the time taken by a function to execute, we can use `performance.now()` to get the start and end times of the function and calculate the difference between them.

```javascript
let startTime = performance.now();

// Function to be measured

let endTime = performance.now();
let timeTaken = endTime - startTime;
```

## Using `console.time()`

The `console.time()` method is used to measure the time taken by a function to execute. It starts a timer with a given label and prints the elapsed time in the console when the timer is stopped.

To measure the time taken by a function to execute, we can use `console.time()` to start and stop the timer and print the elapsed time in the console.

```javascript
console.time("timeTaken");

// Function to be measured

console.timeEnd("timeTaken");
```

## Using `Date.now()`

The `Date.now()` method returns the number of milliseconds elapsed since January 1, 1970 00:00:00 UTC.

To measure the time taken by a function to execute, we can use `Date.now()` to get the start and end times of the function and calculate the difference between them.

```javascript
let startTime = Date.now();

// Function to be measured

let endTime = Date.now();
let timeTaken = endTime - startTime;
```
