---
title: Determine if a variable has been declared and initialized in javascript
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: You can use the typeof operator to check if a variable is defined or not.
---

**Contents**

[TOC]

## Using `typeof` Operator
The `typeof` operator can be used to check if a variable is defined or not. It returns a string indicating the type of the variable. If the variable is not defined, it returns `undefined`.

Example:
```javascript
let myVar;

if (typeof myVar !== 'undefined') {
  console.log('myVar is defined');
} else {
  console.log('myVar is not defined');
}
```

## Using `undefined` Identifier
The `undefined` identifier can also be used to check if a variable is defined or not. It is a global variable and can be used without declaring it.

Example:
```javascript
let myVar;

if (myVar !== undefined) {
  console.log('myVar is defined');
} else {
  console.log('myVar is not defined');
}
```

## Using `in` Operator
The `in` operator can be used to check if a variable is defined or not. It returns `true` if the specified property is in the specified object, otherwise it returns `false`.

Example:
```javascript
let myVar;

if ('myVar' in window) {
  console.log('myVar is defined');
} else {
  console.log('myVar is not defined');
}
```

## Using `hasOwnProperty()` Method
The `hasOwnProperty()` method can be used to check if a variable is defined or not. It returns `true` if the specified property is in the specified object, otherwise it returns `false`.

Example:
```javascript
let myVar;

if (window.hasOwnProperty('myVar')) {
  console.log('myVar is defined');
} else {
  console.log('myVar is not defined');
}
```
