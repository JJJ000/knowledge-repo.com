---
title: How can I use Node.js to make a function wait until a callback has been executed?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-08 00:00:00
updated_at: 2023-02-08 00:00:00
tldr: Use the async/await syntax to have the function wait until the callback is called.
---

**Contents**

[TOC]

#1. Introduction

Node.js is a Javascript runtime environment that enables developers to create server-side applications. It is based on the Chrome V8 Javascript engine and provides an asynchronous, event-driven programming model for developing applications. Node.js is commonly used for web development, but it can also be used for other types of applications.

#2. Using Callbacks

In Node.js, asynchronous functions are usually executed by passing a callback function as an argument. The callback function is invoked when the asynchronous operation is completed. This allows the program to continue executing while the asynchronous operation is being performed.

#3. Waiting for Callbacks

To make a function wait until a callback has been called, the function needs to be wrapped in a Promise. A Promise is an object that represents the eventual completion or failure of an asynchronous operation. The Promise object provides methods for registering callbacks that will be invoked when the asynchronous operation is completed.

#4. Example

For example, the following code shows how to make a function wait until a callback has been called. The function takes a callback as an argument, and returns a Promise that will be resolved when the callback is invoked.

```
function waitForCallback(callback) {
  return new Promise((resolve, reject) => {
    callback(resolve);
  });
}
```
The callback can then be invoked as follows:

```
waitForCallback(function(resolve) {
  // Do something asynchronous
  resolve();
});
```
