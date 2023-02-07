---
title: Pause JavaScript execution before proceeding
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: The setTimeout() function can be used to delay the execution of code for a specified amount of time.
---

**Contents**

[TOC]

## setTimeout()
The `setTimeout()` method can be used to delay the execution of a function for a specified amount of time. This method takes two parameters: a callback function, and the amount of time to delay the execution of the callback function.

## Syntax
The syntax for the `setTimeout()` method is as follows:

```
setTimeout(function, milliseconds);
```

## Examples
Here are some examples of how to use the `setTimeout()` method:

```
// Delay the execution of a function for 5 seconds
setTimeout(function(){
    console.log('Hello World!');
}, 5000);

// Delay the execution of an anonymous function for 3 seconds
setTimeout(() => {
    console.log('Hello World!');
}, 3000);
```

## Conclusion
The `setTimeout()` method can be used to delay the execution of a function for a specified amount of time. This method takes two parameters: a callback function and the amount of time to delay the execution of the callback function.
