---
title: What does the instanceof operator do in javascript?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: The instanceof operator in JavaScript is used to check if an object is an instance of a specified constructor.
---

**Contents**

[TOC]

## Definition
The instanceof operator is a comparison operator in JavaScript that tests whether an object is an instance of a particular constructor.

## Syntax
The syntax for the instanceof operator is:
```
object instanceof constructor
```

## Parameters
- **object**: The object to test.
- **constructor**: The constructor function to test against.

## Example
For example, the following code will return true because the object 'myObject' is an instance of the constructor 'MyConstructor':
```
let myObject = new MyConstructor();
myObject instanceof MyConstructor; // returns true
```
