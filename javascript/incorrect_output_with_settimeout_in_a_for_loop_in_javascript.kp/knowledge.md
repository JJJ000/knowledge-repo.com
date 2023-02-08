---
title: Using settimeout in a for-loop will not produce a sequence of values
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-08 00:00:00
updated_at: 2023-02-08 00:00:00
tldr: No, setTimeout in a for-loop will not print consecutive values due to the asynchronous nature of setTimeout.
---

**Contents**

[TOC]

## Explanation
When using `setTimeout` within a `for` loop, the callback function is queued to be executed after a certain amount of time. However, the `for` loop does not wait for the callback function to be executed before continuing to the next iteration. Therefore, depending on the amount of time specified for the `setTimeout`, the values printed may not be consecutive.

## Example
In the following example, the `for` loop prints the values from 0 to 4. However, the callback function prints the values from 0 to 4 with a delay of 1 second between each print. Therefore, the values printed by the callback function are not consecutive.

```javascript
for (let i = 0; i < 5; i++) {
  console.log(i);
  setTimeout(() => {
    console.log(i);
  }, 1000);
}
```

## Solution
To ensure that the values printed by the callback function are consecutive, the `for` loop needs to wait until the callback function has been executed before continuing to the next iteration. This can be achieved by using `setInterval` instead of `setTimeout` and a `while` loop.

```javascript
let i = 0;
let intervalId = setInterval(() => {
  console.log(i);
  i++;
  if (i === 5) {
    clearInterval(intervalId);
  }
}, 1000);
```
