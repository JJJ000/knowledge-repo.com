---
title: What is the difference between the "for...in" and "for" loops in javascript?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: The `for...in` loop iterates over the properties of an object, while the `for in` loop iterates over the values of an array or object.
---

**Contents**

[TOC]

**For...in**

The for...in statement iterates over the enumerable properties of an object, in arbitrary order. For each distinct property, statements can be executed.

**Syntax**

for (variable in object) {
  statements
}

**Example**

const object = {a: 1, b: 2, c: 3};

for (const property in object) {
  console.log(`${property}: ${object[property]}`);
}

// Output:
// a: 1
// b: 2
// c: 3

**For in**

The for in loop is a combination of the for loop and the in operator. It iterates over all non-Symbol, enumerable properties of an object.

**Syntax**

for (variable in object) {
  statements
}

**Example**

const object = {a: 1, b: 2, c: 3};

for (const property in object) {
  console.log(`${property}: ${object[property]}`);
}

// Output:
// a: 1
// b: 2
// c: 3
