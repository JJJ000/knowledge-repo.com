---
title: Wait until all promises have been fulfilled, regardless of any rejections
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-04 00:00:00
updated_at: 2023-02-04 00:00:00
tldr: Use Promise.allSettled() to wait until all promises complete, regardless of whether they are resolved or rejected.
---

**Contents**

[TOC]

### Using Promise.allSettled

The `Promise.allSettled` method returns a promise that resolves after all of the given promises have either resolved or rejected, with an array of objects that each describes the outcome of each promise. This allows us to wait until all promises have been settled, even if some of them were rejected.

### Example

```
const promise1 = new Promise((resolve, reject) => {
  setTimeout(() => {
    resolve('Promise 1 resolved');
  }, 1000);
});

const promise2 = new Promise((resolve, reject) => {
  setTimeout(() => {
    reject('Promise 2 rejected');
  }, 2000);
});

Promise.allSettled([promise1, promise2])
  .then((results) => {
    results.forEach((result) => {
      console.log(result.status);
    });
  });

// Output:
// 'fulfilled'
// 'rejected'
```

### Using Async/Await

Another way to wait until all promises have been settled, even if some of them were rejected, is to use the `async/await` syntax. This allows us to write asynchronous code that looks and behaves like synchronous code.

### Example

```
async function waitForAllPromises() {
  const promise1 = new Promise((resolve, reject) => {
    setTimeout(() => {
      resolve('Promise 1 resolved');
    }, 1000);
  });

  const promise2 = new Promise((resolve, reject) => {
    setTimeout(() => {
      reject('Promise 2 rejected');
    }, 2000);
  });

  const results = await Promise.allSettled([promise1, promise2]);
  results.forEach((result) => {
    console.log(result.status);
  });
}

waitForAllPromises();

// Output:
// 'fulfilled'
// 'rejected'
```
