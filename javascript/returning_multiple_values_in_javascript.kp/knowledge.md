---
title: How can I return multiple values in javascript?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-03 00:00:00
updated_at: 2023-02-03 00:00:00
tldr: JavaScript functions can return multiple values using arrays, objects, or by using the arguments object.
---

**Contents**

[TOC]

### Using Arrays

Arrays are a great way to return multiple values in JavaScript. We can create an array and add elements to it, then return the array as the function result. 

```javascript
function myFunction() {
  let arr = [];
  arr.push("value1");
  arr.push("value2");
  arr.push("value3");
  return arr;
}

let result = myFunction();
console.log(result); // ["value1", "value2", "value3"]
```

### Using Objects

We can also use objects to return multiple values in JavaScript. We can create an object and add properties to it, then return the object as the function result. 

```javascript
function myFunction() {
  let obj = {};
  obj.prop1 = "value1";
  obj.prop2 = "value2";
  obj.prop3 = "value3";
  return obj;
}

let result = myFunction();
console.log(result); // { prop1: "value1", prop2: "value2", prop3: "value3" }
```

### Using Tuples

Tuples are a great way to return multiple values in JavaScript. We can create a tuple and add elements to it, then return the tuple as the function result. 

```javascript
function myFunction() {
  let tuple = [ "value1", "value2", "value3" ];
  return tuple;
}

let result = myFunction();
console.log(result); // ["value1", "value2", "value3"]
```

### Using Destructuring

Destructuring is another great way to return multiple values in JavaScript. We can create an array or object and return it using destructuring. 

```javascript
function myFunction() {
  let arr = [ "value1", "value2", "value3" ];
  return arr;
}

let [ value1, value2, value3 ] = myFunction();
console.log(value1); // "value1"
console.log(value2); // "value2"
console.log(value3); // "value3"
```
