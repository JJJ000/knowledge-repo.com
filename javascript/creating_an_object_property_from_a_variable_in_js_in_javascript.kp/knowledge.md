---
title: What is the syntax for assigning a variable value to an object property in javascript?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: You can create an object property from a variable value in JavaScript by using bracket notation and the variable name as the property key.
---

**Contents**

[TOC]

## Using Dot Notation

The dot notation is the most common way of creating an object property from a variable value in JavaScript. The syntax for this is `objectName.propertyName = value;`. For example, if you have a variable `myVar` with a value of `"Hello"`, you can create an object property from it like this:

```
var myVar = "Hello";

var myObject = {};
myObject.myVar = myVar;
```

## Using Bracket Notation

The bracket notation is an alternative way of creating an object property from a variable value in JavaScript. The syntax for this is `objectName["propertyName"] = value;`. For example, if you have a variable `myVar` with a value of `"Hello"`, you can create an object property from it like this:

```
var myVar = "Hello";

var myObject = {};
myObject["myVar"] = myVar;
```

## Using Object.defineProperty

The `Object.defineProperty()` method can be used to create an object property from a variable value in JavaScript. The syntax for this is `Object.defineProperty(objectName, propertyName, { value: value });`. For example, if you have a variable `myVar` with a value of `"Hello"`, you can create an object property from it like this:

```
var myVar = "Hello";

var myObject = {};
Object.defineProperty(myObject, "myVar", { value: myVar });
```

## Using Object.assign

The `Object.assign()` method can be used to create an object property from a variable value in JavaScript. The syntax for this is `Object.assign(objectName, {propertyName: value});`. For example, if you have a variable `myVar` with a value of `"Hello"`, you can create an object property from it like this:

```
var myVar = "Hello";

var myObject = {};
Object.assign(myObject, {myVar: myVar});
```
