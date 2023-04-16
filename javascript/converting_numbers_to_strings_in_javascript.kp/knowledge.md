---
title: How can I turn a number into a string in javascript?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: The best way to convert a number to a string in JavaScript is to use the String() constructor or the toString() method.
---

**Contents**

[TOC]

## Number to String

The best way to convert a number to a string in JavaScript is to use the `String()` function. The `String()` function takes any type of input and converts it to a string.

## Examples

Here are some examples of how to use the `String()` function:

```js
let num = 10;
let numAsString = String(num); // numAsString is now "10"

let float = 3.14;
let floatAsString = String(float); // floatAsString is now "3.14"
```

## Other Methods

In addition to the `String()` function, there are other methods for converting a number to a string. These include the `toString()` method, the `Number()` method, and the `String.fromCharCode()` method. Each of these methods has its own advantages and disadvantages, so it is important to consider which one is best for the specific task at hand.
