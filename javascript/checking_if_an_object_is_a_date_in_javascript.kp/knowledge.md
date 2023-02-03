---
title: What is the best way to determine if an object is a date?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-03 00:00:00
updated_at: 2023-02-03 00:00:00
tldr: You can check if an object is a date by using the Date.prototype.toString() method.
---

**Contents**

[TOC]

## Using the Date Constructor

The `Date` constructor can be used to check if an object is a date.

```javascript
var isDate = function(date) {
  return date instanceof Date;
}
```

## Using the toString() Method

The `toString()` method can also be used to check if an object is a date.

```javascript
var isDate = function(date) {
  return Object.prototype.toString.call(date) === '[object Date]';
}
```

## Using the isNaN() Method

The `isNaN()` method can be used to check if an object is a date.

```javascript
var isDate = function(date) {
  return !isNaN(Date.parse(date));
}
```

## Using the getTime() Method

The `getTime()` method can also be used to check if an object is a date.

```javascript
var isDate = function(date) {
  return !isNaN(date.getTime());
}
```
