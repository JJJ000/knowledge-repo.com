---
title: Iterating through a plain JavaScript object with the objects as members
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: You can loop through a plain JavaScript object using the `for...in` loop.
---

**Contents**

[TOC]

##### Using for-in loop

The for-in loop is the most popular way to loop through a plain JavaScript object with the objects as members. It takes the form of `for (variable in object) {...}`. The variable is a property name and the object is the object you want to loop through.

```javascript
const object = {
  a: 1,
  b: 2,
  c: 3
};

for (const property in object) {
  console.log(`${property}: ${object[property]}`);
}

// Output:
// a: 1
// b: 2
// c: 3
```

##### Using Object.keys()

The `Object.keys()` method is another way to loop through a plain JavaScript object with the objects as members. It returns an array containing the object's enumerable properties.

```javascript
const object = {
  a: 1,
  b: 2,
  c: 3
};

const keys = Object.keys(object);

for (const key of keys) {
  console.log(`${key}: ${object[key]}`);
}

// Output:
// a: 1
// b: 2
// c: 3
```

##### Using Object.entries()

The `Object.entries()` method is another way to loop through a plain JavaScript object with the objects as members. It returns an array of key-value pairs for the object's enumerable properties.

```javascript
const object = {
  a: 1,
  b: 2,
  c: 3
};

const entries = Object.entries(object);

for (const [key, value] of entries) {
  console.log(`${key}: ${value}`);
}

// Output:
// a: 1
// b: 2
// c: 3
```

##### Using forEach()

The `forEach()` method is another way to loop through a plain JavaScript object with the objects as members. It calls a function for each key-value pair in the object.

```javascript
const object = {
  a: 1,
  b: 2,
  c: 3
};

Object.entries(object).forEach(([key, value]) => {
  console.log(`${key}: ${value}`);
});

// Output:
// a: 1
// b: 2
// c: 3
```
