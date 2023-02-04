---
title: What is the index of an element in an object array using the indexof method?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-04 00:00:00
updated_at: 2023-02-04 00:00:00
tldr: The indexOf() method can be used to find the index of an object in an array in Javascript.
---

**Contents**

[TOC]

## Definition
The `indexOf()` method is used to search an array for an element and returns its position. It returns -1 if the element is not found.

## Syntax
The syntax for `indexOf()` is as follows:

```
array.indexOf(element)
```

## Example
For example, if we have an array of objects:

```
var arr = [{name: 'John', age: 25}, {name: 'Jane', age: 20}];
```

We can use the `indexOf()` method to find the index of the object with the name 'John':

```
arr.indexOf({name: 'John', age: 25}); // returns 0
```

## Return Value
The `indexOf()` method returns the index of the element in the array if it is found, or -1 if it is not found.
