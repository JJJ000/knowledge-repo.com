---
title: What is the syntax to find the index of an object by its property in javascript?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: You can use the Array.prototype.findIndex() method to get the index of an object by its property in JavaScript.
---

**Contents**

[TOC]

## Using Array.prototype.findIndex() 
The `Array.prototype.findIndex()` method can be used to get the index of an object in an array by its property. 

This method takes a function as an argument which is used to test each element of the array. An object in the array will be passed to the function as an argument and the index of the object is returned if the function returns `true`.

Example:

```javascript
let arr = [
    { name: "John", age: 24 },
    { name: "Jane", age: 22 },
    { name: "Bob", age: 27 }
];

let index = arr.findIndex(obj => obj.name === "Bob");
// index = 2
```

## Using Array.prototype.find()
The `Array.prototype.find()` method can also be used to get the index of an object in an array by its property. 

This method takes a function as an argument which is used to test each element of the array. An object in the array will be passed to the function as an argument and the index of the object is returned if the function returns `true`.

Example:

```javascript
let arr = [
    { name: "John", age: 24 },
    { name: "Jane", age: 22 },
    { name: "Bob", age: 27 }
];

let index = arr.find(obj => obj.name === "Bob");
// index = 2
```

## Using for Loop
A `for` loop can also be used to get the index of an object in an array by its property. 

The loop will iterate over each element in the array and check if the property matches the desired value. If a match is found, the index of the object is returned.

Example:

```javascript
let arr = [
    { name: "John", age: 24 },
    { name: "Jane", age: 22 },
    { name: "Bob", age: 27 }
];

let index;
for (let i = 0; i < arr.length; i++) {
    if (arr[i].name === "Bob") {
        index = i;
        break;
    }
}
// index = 2
```
