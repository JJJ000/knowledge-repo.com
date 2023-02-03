---
title: What is the best way to compare two JavaScript objects to see if they are equal?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-03 00:00:00
updated_at: 2023-02-03 00:00:00
tldr: The equality of two JavaScript objects can be determined by comparing their properties and values with the `===` operator.
---

**Contents**

[TOC]

1. Using `Object.is()` Method
   The `Object.is()` method determines whether two values are the same value. This method is used to determine the equality of two objects in JavaScript. It compares two values and returns a boolean.

2. Using `Object.keys()` Method
   The `Object.keys()` method returns an array of a given object's own enumerable properties. This method can be used to compare two objects and determine if they are equal.

3. Using `JSON.stringify()` Method
   The `JSON.stringify()` method converts a JavaScript object or value to a JSON string. This method can be used to compare two objects and determine if they are equal.

4. Using `Object.assign()` Method
   The `Object.assign()` method is used to copy the values of all enumerable own properties from one or more source objects to a target object. This method can be used to compare two objects and determine if they are equal.
