---
title: Obtaining a selection of properties from a JavaScript object
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-04 00:00:00
updated_at: 2023-02-04 00:00:00
tldr: Use the Object.keys() method to get an array of the object`s keys, then use array methods such as filter() or map() to get a subset of the object`s properties.
---

**Contents**

[TOC]

## 1. Using Object.keys()

Object.keys() returns an array of a given object's own enumerable property names, in the same order as we get with a normal loop.

We can use this array to create a new object with only the properties we want.

```javascript
// Example object
let obj = {
  name: "John Doe",
  age: 32,
  city: "New York"
};

// Create an array of only the keys we want
let keys = ["name", "age"];

// Create a new object with only the desired properties
let newObj = {};
keys.forEach(key => {
  newObj[key] = obj[key];
});

// newObj now contains only the properties we wanted
console.log(newObj); // {name: "John Doe", age: 32}
```

## 2. Using Object.assign()

Object.assign() allows us to copy the values of all enumerable own properties from one or more source objects to a target object.

We can use this to create a new object with only the properties we want.

```javascript
// Example object
let obj = {
  name: "John Doe",
  age: 32,
  city: "New York"
};

// Create an object with only the properties we want
let newObj = {};
Object.assign(newObj, obj, {name: obj.name, age: obj.age});

// newObj now contains only the properties we wanted
console.log(newObj); // {name: "John Doe", age: 32}
```

## 3. Using Destructuring

ES6 destructuring allows us to extract data from objects and arrays into distinct variables.

We can use this to create a new object with only the properties we want.

```javascript
// Example object
let obj = {
  name: "John Doe",
  age: 32,
  city: "New York"
};

// Create an object with only the properties we want
let {name, age} = obj;
let newObj = {name, age};

// newObj now contains only the properties we wanted
console.log(newObj); // {name: "John Doe", age: 32}
```

## 4. Using Lodash

Lodash is a JavaScript library that provides utility functions for common programming tasks.

We can use the _.pick() function to create a new object with only the properties we want.

```javascript
// Example object
let obj = {
  name: "John Doe",
  age: 32,
  city: "New York"
};

// Create an object with only the properties we want
let newObj = _.pick(obj, ["name", "age"]);

// newObj now contains only the properties we wanted
console.log(newObj); // {name: "John Doe", age: 32}
```
