---
title: Setinterval is a function that runs a specified function at a set interval, while settimeout is a function that runs a specified function after a set amount of time
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: setInterval runs a function repeatedly at a given interval, while setTimeout runs a function once after a given interval.
---

**Contents**

[TOC]

## setInterval

`setInterval` is a function in JavaScript that executes a given function at a set interval. It takes two parameters: a function and a delay in milliseconds. The function will be executed every time the delay has passed.

## setTimeout

`setTimeout` is a function in JavaScript that executes a given function after a set amount of time. It takes two parameters: a function and a delay in milliseconds. The function will be executed once after the delay has passed.

## Difference

The primary difference between `setInterval` and `setTimeout` is that `setInterval` will execute the given function repeatedly at the given interval, whereas `setTimeout` will only execute the given function once after the given interval.

## Use Cases

`setInterval` is useful for tasks that need to be executed repeatedly, such as checking for updates or refreshing the page. `setTimeout` is useful for tasks that need to be executed once after a certain amount of time, such as displaying a message after a certain amount of time or redirecting the user to a different page after a certain amount of time.
