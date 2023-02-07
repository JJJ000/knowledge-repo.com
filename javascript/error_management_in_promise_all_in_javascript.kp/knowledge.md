---
title: Dealing with mistakes in promise.all
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: Errors in Promise.all can be handled by using the catch method on the Promise.all call.
---

**Contents**

[TOC]

##### Catching Errors

The most straightforward way of handling errors in Promise.all is to use the `.catch()` method. This method takes a callback that will be called if any of the promises in the Promise.all fails. The callback will receive the error that caused the promise to fail.

```js
Promise.all([promise1, promise2, promise3])
  .catch(err => {
    // Handle the error here
  });
```

##### Handling Individual Errors

Another way to handle errors in Promise.all is to use the `.then()` method. This method takes a callback that will be called when all of the promises in the Promise.all are resolved. The callback will receive an array of the results of each promise.

If any of the promises fail, the result of that promise will be an error. You can then use the array of results to inspect each promise individually and handle the errors accordingly.

```js
Promise.all([promise1, promise2, promise3])
  .then(results => {
    results.forEach(result => {
      if (result instanceof Error) {
        // Handle the error here
      }
    });
  });
```

##### Using try/catch

Another way to handle errors in Promise.all is to use a try/catch block. This allows you to wrap the entire Promise.all in a try/catch block, and handle any errors that occur.

```js
try {
  await Promise.all([promise1, promise2, promise3]);
} catch (err) {
  // Handle the error here
}
```
