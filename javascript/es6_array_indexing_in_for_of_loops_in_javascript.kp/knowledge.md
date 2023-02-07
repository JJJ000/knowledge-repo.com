---
title: Iterating through an es6 array's elements using a for-of loop
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: The index of the current element can be accessed using the `index` property of the iterator object.
---

**Contents**

[TOC]

# Using Array.entries()

The ES6 `Array.entries()` method returns an array iterator object with key/value pairs. This allows us to access the index of the array element in the for-of loop.

```
let arr = [1,2,3];

for (let [index, element] of arr.entries()) {
  console.log(index, element);
}
```

# Using Array.keys()

The ES6 `Array.keys()` method returns an array iterator object with the keys of the array elements. This allows us to access the index of the array element in the for-of loop.

```
let arr = [1,2,3];

for (let index of arr.keys()) {
  console.log(index, arr[index]);
}
```

# Using for-in loop

The traditional for-in loop can also be used to access the index of the array element in the for-of loop. 

```
let arr = [1,2,3];

for (let index in arr) {
  console.log(index, arr[index]);
}
```

# Using forEach()

The ES5 `Array.forEach()` method can also be used to access the index of the array element in the for-of loop. 

```
let arr = [1,2,3];

arr.forEach((element, index) => {
  console.log(index, element);
});
```
