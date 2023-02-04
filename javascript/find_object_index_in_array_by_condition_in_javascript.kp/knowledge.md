---
title: Find the index of the object in an array that meets a certain criteria
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-04 00:00:00
updated_at: 2023-02-04 00:00:00
tldr: Use the Array.prototype.findIndex() method to get the index of an object inside an array, matching a condition.
---

**Contents**

[TOC]

## Using the `findIndex` Method

The `findIndex` method is a useful tool for finding the index of an object inside an array that matches a condition. It takes in a callback function as an argument, which is used to test each element of the array. If the condition is met, the index of the element is returned.

Example:

```javascript
const arr = [
  { name: "John", age: 21 },
  { name: "Jane", age: 24 },
  { name: "Bob", age: 27 }
];

const index = arr.findIndex(person => person.name === "Jane");

console.log(index); // 1
```

In the example above, the index of the object with the name `Jane` is returned.

## Using the `forEach` Method

Another approach to finding the index of an object inside an array is to use the `forEach` method. This method iterates over the array and calls a callback function for each element. The index of the element can be used in the callback function to test the condition and return the index if it is met.

Example:

```javascript
const arr = [
  { name: "John", age: 21 },
  { name: "Jane", age: 24 },
  { name: "Bob", age: 27 }
];

let index;

arr.forEach((person, i) => {
  if (person.name === "Jane") {
    index = i;
  }
});

console.log(index); // 1
```

## Using the `for` Loop

The `for` loop is a classic approach to iterating over an array and testing a condition. The index of the element can be used in the loop to test the condition and return the index if it is met.

Example:

```javascript
const arr = [
  { name: "John", age: 21 },
  { name: "Jane", age: 24 },
  { name: "Bob", age: 27 }
];

let index;

for (let i = 0; i < arr.length; i++) {
  if (arr[i].name === "Jane") {
    index = i;
    break;
  }
}

console.log(index); // 1
```

## Using the `map` Method

The `map` method is another approach to finding the index of an object inside an array. It iterates over the array and calls a callback function for each element. The index of the element can be used in the callback function to test the condition and return the index if it is met.

Example:

```javascript
const arr = [
  { name: "John", age: 21 },
  { name: "Jane", age: 24 },
  { name: "Bob", age: 27 }
];

const index = arr.map((person, i) => {
  if (person.name === "Jane") {
    return i;
  }
})[0];

console.log(index); // 1
```
