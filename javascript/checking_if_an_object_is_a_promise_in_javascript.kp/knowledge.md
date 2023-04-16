---
title: What is the best way to determine if an object is a promise?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: You can check if an object is a Promise by using the `Promise.resolve()` method.
---

**Contents**

[TOC]

## Using the `instanceof` operator

The `instanceof` operator can be used to check if an object is an instance of a given constructor. In the case of Promises, we can use it to check if an object is a Promise by checking if it is an instance of the `Promise` constructor:

```javascript
const myPromise = new Promise((resolve, reject) => {
  // promise code here
});

console.log(myPromise instanceof Promise); // true
```

## Using the `then` method

Another way to check if an object is a Promise is to check if it has a `then` method. Promises have a `then` method which can be used to add callbacks for when the Promise is resolved or rejected. If the object has a `then` method, it is likely a Promise:

```javascript
const myPromise = new Promise((resolve, reject) => {
  // promise code here
});

console.log(typeof myPromise.then === 'function'); // true
```

## Using a polyfill

If the environment does not support Promises, you can use a polyfill to add Promise support. In this case, you can use the polyfill to check if an object is a Promise:

```javascript
// polyfill code here

const myPromise = new Promise((resolve, reject) => {
  // promise code here
});

console.log(myPromise.__isPromise); // true
```

## Using a library

If you are using a library such as [Bluebird](https://github.com/petkaantonov/bluebird), you can use the library's methods to check if an object is a Promise:

```javascript
const myPromise = new Promise((resolve, reject) => {
  // promise code here
});

console.log(Bluebird.is(myPromise)); // true
```
