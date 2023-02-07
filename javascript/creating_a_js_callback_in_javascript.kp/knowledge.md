---
title: Write a custom JavaScript function to use as a callback
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: A custom callback in JavaScript is a function that is passed as an argument to another function and is executed asynchronously when the other function is completed.
---

**Contents**

[TOC]

**Section 1: Defining a Callback Function**

A callback function is a function that is passed as an argument to another function, to be invoked at a later time.

**Section 2: Creating a Custom Callback Function**

To create a custom callback function, you must first define the function. This can be done as follows:

```javascript
function customCallback(param1, param2) {
  // do something with param1 and param2
}
```

**Section 3: Passing the Callback Function as an Argument**

Once the callback function is defined, it can be passed as an argument to another function. This can be done as follows:

```javascript
function anotherFunction(param1, param2, callback) {
  // do something with param1 and param2
  callback(param1, param2);
}
```

**Section 4: Invoking the Callback Function**

The callback function can then be invoked by calling the anotherFunction() function and passing the customCallback() function as an argument. This can be done as follows:

```javascript
anotherFunction(param1, param2, customCallback);
```
