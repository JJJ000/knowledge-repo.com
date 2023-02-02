---
title: What is the process for determining if one string begins with another?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-02 00:00:00
updated_at: 2023-02-02 00:00:00
tldr: You can use the startsWith() method to check if a string starts with another string in JavaScript.
---

**Contents**

[TOC]

#1. Using the `startsWith()` Method

The `startsWith()` method checks whether a string begins with the characters of a specified string, returning true or false as appropriate.

## Syntax

```
string.startsWith(searchString[, position])
```

## Examples

```
var str = "Hello world, welcome to the universe.";

console.log(str.startsWith("Hello")); // true
console.log(str.startsWith("world", 6)); // true
console.log(str.startsWith("world", 7)); // false
```

#2. Using the `indexOf()` Method

The `indexOf()` method returns the index within the calling string object of the first occurrence of the specified value, starting the search at fromIndex. Returns -1 if the value is not found.

## Syntax

```
string.indexOf(searchValue[, fromIndex])
```

## Examples

```
var str = "Hello world, welcome to the universe.";

console.log(str.indexOf("Hello") === 0); // true
console.log(str.indexOf("world", 6) === 6); // true
console.log(str.indexOf("world", 7) === -1); // false
```
