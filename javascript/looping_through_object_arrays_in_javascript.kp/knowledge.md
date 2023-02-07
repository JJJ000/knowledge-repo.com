---
title: Iterating over an array of objects and accessing their properties
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: Use a for loop to iterate through the array and access the properties of each object using dot notation or bracket notation.
---

**Contents**

[TOC]

### Using `for` Loop

The most common way to loop through an array containing objects is to use a `for` loop. We can use the `for` loop to iterate over the array and access the properties of each object.

```js
var arr = [{name: 'John', age: 20}, {name: 'Bob', age: 30}];

for (var i = 0; i < arr.length; i++) {
  console.log(arr[i].name);
  console.log(arr[i].age);
}
```

### Using `forEach` Method

Another way to loop through an array containing objects is to use the `forEach` method. The `forEach` method takes a callback function as an argument and calls it once for each element in the array.

```js
var arr = [{name: 'John', age: 20}, {name: 'Bob', age: 30}];

arr.forEach(function(item) {
  console.log(item.name);
  console.log(item.age);
});
```

### Using `for-of` Loop

The `for-of` loop is another way to loop through an array containing objects. The `for-of` loop is a new loop introduced in ES6 and it is used to iterate over the values of an iterable object.

```js
var arr = [{name: 'John', age: 20}, {name: 'Bob', age: 30}];

for (const item of arr) {
  console.log(item.name);
  console.log(item.age);
}
```

### Using `for-in` Loop

The `for-in` loop is another way to loop through an array containing objects. The `for-in` loop is used to iterate over the properties of an object.

```js
var arr = [{name: 'John', age: 20}, {name: 'Bob', age: 30}];

for (const key in arr) {
  console.log(arr[key].name);
  console.log(arr[key].age);
}
```
