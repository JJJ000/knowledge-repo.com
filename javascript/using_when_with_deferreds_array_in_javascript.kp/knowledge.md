---
title: Provide an array of deferreds to $.when()
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-04 00:00:00
updated_at: 2023-02-04 00:00:00
tldr: $.when() will execute a function when all of the Deferreds in the array have been resolved.
---

**Contents**

[TOC]

**Section 1: What is $.when()?**

$.when() is a jQuery method that allows you to execute multiple Deferred objects in a single call. It takes a single Deferred object or an array of Deferred objects as its argument and returns a new Promise object that is resolved when all of the Deferred objects in the array have been resolved.

**Section 2: How to Pass an Array of Deferreds to $.when()**

To pass an array of Deferreds to $.when(), you must first create an array that contains all of the Deferred objects that you wish to execute. Then, you must pass the array to the $.when() method as the first argument. 

**Section 3: Example**

For example, if you have two Deferred objects, deferred1 and deferred2, you can pass them both to $.when() by creating an array that contains them and passing it as the first argument to $.when():

```
var deferreds = [deferred1, deferred2];
$.when(deferreds).then(function() {
    // Do something when both deferreds have been resolved
});
```

**Section 4: Benefits of Using $.when()**

Using $.when() to execute multiple Deferred objects in a single call has several benefits. First, it allows you to easily execute multiple asynchronous operations in parallel, which can improve the performance of your code. Second, it allows you to easily handle errors that occur during the execution of the Deferred objects, as the Promise object returned by $.when() will be rejected if any of the Deferred objects in the array are rejected. Finally, it allows you to easily chain multiple asynchronous operations together, as the Promise object returned by $.when() will be resolved when all of the Deferred objects in the array have been resolved.
