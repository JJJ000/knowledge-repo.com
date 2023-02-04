---
title: What is the best way to pause execution in Node.js (javascript) for a certain amount of time?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-04 00:00:00
updated_at: 2023-02-04 00:00:00
tldr: Use the setTimeout() function to pause execution for a specified amount of time.
---

**Contents**

[TOC]

## Using setTimeout

The `setTimeout()` function is a built-in JavaScript function that allows you to pause execution of a script for a specified amount of time. The syntax for `setTimeout()` is as follows:

```javascript
setTimeout(function, delay);
```

Where `function` is the function to be executed after the specified `delay` in milliseconds. For example, to wait for 5 seconds before executing a function:

```javascript
setTimeout(myFunction, 5000);
```

## Using setInterval

The `setInterval()` function is similar to the `setTimeout()` function, but it allows you to execute a function repeatedly, at a specified interval. The syntax for `setInterval()` is as follows:

```javascript
setInterval(function, delay);
```

Where `function` is the function to be executed at the specified `delay` in milliseconds. For example, to execute a function every 5 seconds:

```javascript
setInterval(myFunction, 5000);
```

## Using async/await

The `async` and `await` keywords are a way to write asynchronous code in a more synchronous-like manner. The syntax for using `async/await` to wait for a specified amount of time is as follows:

```javascript
async function myFunction() {
  await new Promise(resolve => setTimeout(resolve, 5000));
  // code to be executed after 5 seconds
}
```

Where the `setTimeout()` function is used to wait for 5 seconds before executing the code inside the `myFunction()` function.
