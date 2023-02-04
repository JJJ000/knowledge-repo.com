---
title: What is the process for retrieving the results of a preceding promise in a .then() chain?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-04 00:00:00
updated_at: 2023-02-04 00:00:00
tldr: You can access previous promise results in a .then() chain by using the resolved value of the previous promise as an argument for the next .then() call.
---

**Contents**

[TOC]

## Accessing Previous Promise Results

When working with promises, it is possible to access the results of a previous promise in the `.then()` chain. This can be done by simply returning the result of the previous promise in the `.then()` callback.

## Example

The following example shows how to access the result of a previous promise in the `.then()` chain.

```javascript
Promise.resolve('hello')
  .then(result => {
    console.log('First promise result:', result);
    return 'world';
  })
  .then(result => {
    console.log('Second promise result:', result);
  });
```

In this example, the `.then()` callback of the first promise returns the string `'world'`, which is then passed to the second `.then()` callback.

## Further Reading

For more information on promises and accessing the results of previous promises, please see the following resources:

- [MDN - Using Promises](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Using_promises)
- [JavaScript.info - Promises](https://javascript.info/promise-basics)
