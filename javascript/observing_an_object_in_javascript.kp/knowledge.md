---
title: Observe an object
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: You can watch an object in Javascript by using the Object.observe() method.
---

**Contents**

[TOC]

1. Using `Object.observe()`:
   - `Object.observe()` is a method that can be used to watch an object for changes. It takes two arguments: the object to watch and a callback function to execute when a change is detected. The callback function will be called with an array of changes that have occurred.

2. Using `Proxy`:
   - `Proxy` is an ES6 feature that can be used to create a proxy object that wraps an existing object. It takes two arguments: the object to wrap and an object of handlers that specify what to do when an operation is performed on the proxy object. By using the `set` handler, you can watch for changes to the proxy object and execute a callback function when a change is detected.

3. Using `setInterval()`:
   - `setInterval()` is a method that can be used to execute a function repeatedly at a specified interval. By using this method, you can check for changes to an object periodically and execute a callback function when a change is detected.

4. Using `setTimeout()`:
   - `setTimeout()` is a method that can be used to execute a function once after a specified amount of time has elapsed. By using this method, you can check for changes to an object after a certain amount of time has elapsed and execute a callback function when a change is detected.
