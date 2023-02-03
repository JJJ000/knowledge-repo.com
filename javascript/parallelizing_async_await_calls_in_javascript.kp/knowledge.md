---
title: Invoke async/await functions concurrently
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-03 00:00:00
updated_at: 2023-02-03 00:00:00
tldr: You can use the `Promise.all` method to call async/await functions in parallel.
---

**Contents**

[TOC]

### Using Promise.all()
Promise.all() is a way to call async/await functions in parallel. It takes an array of promises and returns a single promise that resolves when all of the promises in the array have been resolved.

```
const promise1 = asyncFunc1();
const promise2 = asyncFunc2();
const promise3 = asyncFunc3();

Promise.all([promise1, promise2, promise3]).then(values => {
  // All async functions have resolved
  console.log(values);
});
```

### Using async/await
Another way to call async/await functions in parallel is to use the async/await syntax. This syntax allows you to await multiple promises at once.

```
const [result1, result2, result3] = await Promise.all([
  asyncFunc1(),
  asyncFunc2(),
  asyncFunc3()
]);

console.log(result1, result2, result3);
```

### Using for-await-of
The for-await-of statement can be used to call async/await functions in parallel. This syntax is similar to the for-of statement, but it allows you to await the results of each iteration.

```
const promises = [asyncFunc1(), asyncFunc2(), asyncFunc3()];
const results = [];

for await (const result of promises) {
  results.push(result);
}

console.log(results);
```

### Using Promise.allSettled()
Promise.allSettled() is a new way to call async/await functions in parallel. This method takes an array of promises and returns a single promise that resolves when all of the promises in the array have been settled (either fulfilled or rejected).

```
const promise1 = asyncFunc1();
const promise2 = asyncFunc2();
const promise3 = asyncFunc3();

Promise.allSettled([promise1, promise2, promise3]).then(values => {
  // All async functions have settled
  console.log(values);
});
```
