---
title: Find the index of a loop iteration using the for...of syntax in javascript
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: The loop counter/index can be accessed using the variable declared in the for...of syntax.
---

**Contents**

[TOC]

## Using a Traditional For Loop

When using a traditional for loop, you can use the `i` variable to keep track of the loop counter/index.

```javascript
for (let i = 0; i < arr.length; i++) {
  console.log(arr[i]);
}
```

## Using For...Of

When using a for...of loop, you can use the `index` variable to keep track of the loop counter/index.

```javascript
let index = 0;
for (let element of arr) {
  console.log(element);
  index++;
}
```
