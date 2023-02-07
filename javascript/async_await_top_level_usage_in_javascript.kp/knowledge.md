---
title: What is the best way to implement async/await at the highest level?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: You can use the top level await operator in Javascript to use async/await at the top level.
---

**Contents**

[TOC]

### Using IIFE

One way to use async/await at the top level is to wrap the code in an Immediately Invoked Function Expression (IIFE). This is a function that is declared and immediately called. The code within the function can then use async/await.

```js
(async () => {
  // code using async/await
})();
```

### Using Async/Await with Promises

Another way to use async/await at the top level is to wrap the code in a Promise. This can be done by using the `Promise.resolve()` method. The code within the Promise can then use async/await.

```js
Promise.resolve().then(async () => {
  // code using async/await
});
```

### Using Async/Await with Generators

Another way to use async/await at the top level is to wrap the code in a generator function. This can be done by using the `Generator.next()` method. The code within the generator can then use async/await.

```js
Generator.next().then(async () => {
  // code using async/await
});
```

### Using Async/Await with Event Listeners

Another way to use async/await at the top level is to wrap the code in an event listener. This can be done by using the `addEventListener()` method. The code within the event listener can then use async/await.

```js
document.addEventListener('DOMContentLoaded', async () => {
  // code using async/await
});
```
