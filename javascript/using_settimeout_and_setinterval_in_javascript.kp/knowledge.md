---
title: What is the difference between settimeout and setinterval?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-03 00:00:00
updated_at: 2023-02-03 00:00:00
tldr: setTimeout is used to execute a function once after a specified amount of time, while setInterval is used to execute a function repeatedly at a specified interval.
---

**Contents**

[TOC]

### setTimeout
setTimeout is a method in Javascript that is used to execute a function after a specified amount of time. It takes two parameters: a function to be executed and a delay in milliseconds.

### Syntax
```
setTimeout(function, delay);
```

### Usage
setTimeout can be used to delay the execution of a function. This can be useful for animation, delaying a request, or any other task that needs to be done after a certain amount of time.

### Example
```
setTimeout(function(){
    console.log("Hello World!");
}, 2000);
```
This code will log "Hello World!" to the console after a two second delay.
