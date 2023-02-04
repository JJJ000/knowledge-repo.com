---
title: What is the content of the JavaScript object?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-04 00:00:00
updated_at: 2023-02-04 00:00:00
tldr: To access and print the content of a JavaScript object, you can use the dot notation or bracket notation to access the object`s properties and then use the console.log() function to print the values.
---

**Contents**

[TOC]

### Using `for...in` Loop

```javascript
let obj = {
  name: "John",
  age: 30,
  city: "New York"
};

for (let key in obj) {
  console.log(key + ": " + obj[key]);
}
```

### Using `Object.keys()`

```javascript
let obj = {
  name: "John",
  age: 30,
  city: "New York"
};

let keys = Object.keys(obj);

keys.forEach(function(key) {
  console.log(key + ": " + obj[key]);
});
```

### Using `Object.entries()`

```javascript
let obj = {
  name: "John",
  age: 30,
  city: "New York"
};

let entries = Object.entries(obj);

entries.forEach(entry => {
  let key = entry[0];
  let value = entry[1];

  console.log(key + ": " + value);
});
```

### Using `Object.values()`

```javascript
let obj = {
  name: "John",
  age: 30,
  city: "New York"
};

let values = Object.values(obj);

values.forEach(value => {
  console.log(value);
});
```
