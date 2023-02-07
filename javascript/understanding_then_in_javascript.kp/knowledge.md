---
title: What is the purpose of the then() method in javascript?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: The function then() is used to specify a callback function to be executed after a Promise is fulfilled or rejected.
---

**Contents**

[TOC]

# Definition
The then() method is used to register a callback function to be executed when a Promise is resolved. It takes two arguments: callback functions for the success and failure cases of the Promise.

# Syntax
The syntax for the then() method is as follows:

promise.then(onFulfilled, onRejected)

# Parameters
The parameters of the then() method are as follows:

onFulfilled: A Function called when the Promise is resolved. This function has one argument, the fulfillment value of the Promise.

onRejected: A Function called when the Promise is rejected. This function has one argument, the rejection reason of the Promise.

# Examples
Here is an example of using the then() method with a Promise:

let promise = new Promise((resolve, reject) => {
  // do something
  if (/* condition is true */) {
    resolve('Success!');
  } else {
    reject('Failure!');
  }
});

promise.then(
  (result) => {
    console.log(result); // 'Success!'
  },
  (error) => {
    console.log(error); // 'Failure!'
  }
);
