---
title: What is the purpose of using "array.prototype.slice.call"?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-04 00:00:00
updated_at: 2023-02-04 00:00:00
tldr: Array.prototype.slice.call is a method used to convert an array-like object into an array.
---

**Contents**

[TOC]

### What is `Array.prototype.slice.call`?

`Array.prototype.slice.call` is a method used to convert an array-like object into an array. It is a part of the JavaScript Array prototype, meaning it is available to all arrays.

### How Does it Work?

The `Array.prototype.slice.call` method takes an array-like object as its argument and returns a shallow copy of the array-like object as an array. The shallow copy is created by calling the `slice` method on the array-like object, and then passing the resulting array to the `call` method.

This method works by looping through the elements of the array-like object and copying them into a new array. The new array is then returned as the result.

### Examples

For example, if we have an array-like object such as `arguments` in a function, we can use `Array.prototype.slice.call` to convert it into an array:

```javascript
function myFunc() {
  let args = Array.prototype.slice.call(arguments);
  // args is now an array
}
```

We can also use `Array.prototype.slice.call` to convert a NodeList into an array:

```javascript
let nodeList = document.querySelectorAll('div');
let divs = Array.prototype.slice.call(nodeList);
// divs is now an array
```

### Advantages

Using `Array.prototype.slice.call` to convert array-like objects into arrays has the advantage of making it easier to work with the data. Since arrays are a standard data type in JavaScript, they can be manipulated and iterated over with ease. This makes it easier to work with array-like objects in a consistent manner.
