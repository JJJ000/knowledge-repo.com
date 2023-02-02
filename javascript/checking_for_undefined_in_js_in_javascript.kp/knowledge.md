---
title: What is the best way to determine if a variable is undefined in javascript?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-02 00:00:00
updated_at: 2023-02-02 00:00:00
tldr: Check for undefined using the strict equality operator (===) to compare the variable to undefined.
---

**Contents**

[TOC]

## Using typeof

The `typeof` operator can be used to check if a value is `undefined`.

```javascript
var myVar;

if (typeof myVar === "undefined") {
  console.log("myVar is undefined");
}
```

## Using Comparison

The `undefined` value can also be checked by comparing it to `undefined` directly.

```javascript
var myVar;

if (myVar === undefined) {
  console.log("myVar is undefined");
}
```

## Using Strict Equality

The `===` operator can be used to check for strict equality, which will also return `true` if the value is `undefined`.

```javascript
var myVar;

if (myVar === undefined) {
  console.log("myVar is undefined");
}
```

## Using Object Property

The `undefined` value can also be checked by accessing a non-existent property of an object.

```javascript
var myObj = {};

if (myObj.myProp === undefined) {
  console.log("myProp is undefined");
}
```
