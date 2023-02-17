---
title: Add an item to a JavaScript array
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-17 00:00:00
updated_at: 2023-02-17 00:00:00
tldr: You can use the JavaScript push() method to add an element to an array stored in a JSON object.
---

**Contents**

[TOC]

##### Section 1: Overview
The `push` method is used to add one or more elements to the end of an array. It modifies the array in place and returns the new length of the array.

##### Section 2: Adding Elements to JSON Arrays
JSON arrays are used to store a collection of values. Elements can be added to a JSON array using the `push` method.

##### Section 3: Syntax
The syntax for the `push` method is as follows:
```
array.push(element1[, ...[, elementN]])
```

##### Section 4: Example
The following example adds two elements to a JSON array:
```
let myArray = [1, 2, 3];
myArray.push(4, 5);

// myArray is now [1, 2, 3, 4, 5]
```
