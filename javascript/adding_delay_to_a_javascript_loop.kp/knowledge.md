---
title: What is the best way to introduce a time delay in a JavaScript loop?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-04 00:00:00
updated_at: 2023-02-04 00:00:00
tldr: Use the setTimeout() method to add a delay in a JavaScript loop.
---

**Contents**

[TOC]

1. Using `setTimeout()`:

```js
for (let i = 0; i < 10; i++) {
  setTimeout(function() {
    console.log(i);
  }, i * 1000);
}
```

2. Using `setInterval()`:

```js
let i = 0;
let intervalId = setInterval(function() {
  console.log(i);
  i++;
  if (i > 10) {
    clearInterval(intervalId);
  }
}, 1000);
```

3. Using `async/await`:

```js
async function loopWithDelay() {
  for (let i = 0; i < 10; i++) {
    await new Promise(resolve => setTimeout(resolve, 1000));
    console.log(i);
  }
}
```

4. Using `Promise.all()`:

```js
let promises = [];

for (let i = 0; i < 10; i++) {
  promises.push(new Promise(resolve => setTimeout(resolve, i * 1000)));
}

Promise.all(promises).then(function() {
  console.log('all done');
});
```
