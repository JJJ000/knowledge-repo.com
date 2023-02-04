---
title: Take out the last element from the array
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-04 00:00:00
updated_at: 2023-02-04 00:00:00
tldr: array.pop() removes the last item from an array in Javascript.
---

**Contents**

[TOC]

## Method 1 
Using `pop()`:

```
let arr = [1, 2, 3, 4, 5];
arr.pop(); // Removes the last item (5)
console.log(arr); // [1, 2, 3, 4]
```

## Method 2 
Using `splice()`:

```
let arr = [1, 2, 3, 4, 5];
arr.splice(-1, 1); // Removes the last item (5)
console.log(arr); // [1, 2, 3, 4]
```

## Method 3 
Using `slice()`:

```
let arr = [1, 2, 3, 4, 5];
arr = arr.slice(0, -1); // Removes the last item (5)
console.log(arr); // [1, 2, 3, 4]
```

## Method 4 
Using `shift()`:

```
let arr = [1, 2, 3, 4, 5];
arr.shift(); // Removes the first item (1)
console.log(arr); // [2, 3, 4, 5]
```
