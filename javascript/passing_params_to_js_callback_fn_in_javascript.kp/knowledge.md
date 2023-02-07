---
title: Passing arguments to a JavaScript callback function
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: Passing parameters to a callback function in JavaScript can be done by providing the parameters as arguments when calling the callback function.
---

**Contents**

[TOC]

##### Definition
A callback function is a function that is passed as an argument to another function and is executed after some kind of event occurs or some kind of operation is completed.

##### Passing Parameters
Parameters can be passed to a callback function in the same way that they are passed to any other function. The parameters are specified when the callback is defined, and they are passed to the callback when it is invoked.

##### Example
For example, consider the following code:

```javascript
function myCallback(param1, param2) {
  console.log(param1 + param2);
}

function doSomething(a, b, callback) {
  callback(a, b);
}

doSomething(1, 2, myCallback);
```

In this example, the `doSomething` function takes three arguments: `a`, `b`, and a callback function. When `doSomething` is invoked, it calls the `myCallback` function and passes it the arguments `a` and `b`. The `myCallback` function then logs the sum of `a` and `b` to the console.

##### Conclusion
In summary, parameters can be passed to a callback function in the same way that they are passed to any other function. The parameters are specified when the callback is defined, and they are passed to the callback when it is invoked.
