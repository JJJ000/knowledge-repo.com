---
title: A function that checks if a value is a number, similar to jquery's isnumeric() but using pure javascript
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: The isFinite() function can be used to check if a value is a finite number.
---

**Contents**

[TOC]

## Regular Expression

The following function uses a regular expression to check if a value is numeric:

```js
function isNumeric(value) {
    return /^\d+$/.test(value);
}
```

## Using the isFinite() Function

The `isFinite()` function can be used to check if a value is numeric:

```js
function isNumeric(value) {
    return isFinite(value);
}
```

## Using the parseFloat() Function

The `parseFloat()` function can also be used to check if a value is numeric:

```js
function isNumeric(value) {
    return !isNaN(parseFloat(value)) && isFinite(value);
}
```

## Using the Number() Constructor

The `Number()` constructor can also be used to check if a value is numeric:

```js
function isNumeric(value) {
    return !isNaN(Number(value));
}
```
