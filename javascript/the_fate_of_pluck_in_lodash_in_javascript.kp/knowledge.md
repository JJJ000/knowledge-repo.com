---
title: What is the current status of the lodash _.pluck function?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-08 00:00:00
updated_at: 2023-02-08 00:00:00
tldr: Lodash`s \_.pluck function has been replaced by the native Javascript Array.prototype.map() method.
---

**Contents**

[TOC]

# Deprecated

Lodash's `_.pluck` method was deprecated in version 4.17.0 in favor of `_.map`.

# Replacement

The `_.map` method is a more versatile replacement for `_.pluck`. It allows users to iterate over arrays and objects and apply a transformation to each element. This can include extracting a property from an object, which was the primary purpose of `_.pluck`.

# Syntax

The syntax for `_.map` is as follows: 

`_.map(collection, [iteratee=_.identity])`

The `iteratee` argument can be a function that takes three arguments: `value`, `index`, and `collection`. This allows users to specify the transformation they would like to apply to each element in the collection.

# Example

For example, if you have an array of objects and would like to extract a property from each object, you can use `_.map` as follows:

```javascript
const users = [
  { name: 'John', age: 30 },
  { name: 'Jane', age: 20 },
  { name: 'Bob', age: 40 }
];

const names = _.map(users, 'name');

// names = ['John', 'Jane', 'Bob']
```
