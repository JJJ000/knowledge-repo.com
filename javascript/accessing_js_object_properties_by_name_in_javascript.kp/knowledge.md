---
title: Accessing a variable property in a JavaScript object using its name as a string
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-04 00:00:00
updated_at: 2023-02-04 00:00:00
tldr: You can use bracket notation to access a JavaScript object`s property by name as a string.
---

**Contents**

[TOC]

## Dot Notation

The most common way to access a variable property by name as a string in JavaScript is to use dot notation. This method requires the name of the property to be known and written as a literal string. 

For example, if an object called `person` has a property called `name`, it could be accessed in the following way:

```javascript
person.name
```

## Bracket Notation

Another way to access a variable property by name as a string in JavaScript is to use bracket notation. This method allows the name of the property to be stored in a variable or passed as an argument.

For example, if an object called `person` has a property called `name`, it could be accessed in the following way:

```javascript
var propertyName = "name";
person[propertyName]
```

## Object.keys()

A third way to access a variable property by name as a string in JavaScript is to use the `Object.keys()` method. This method returns an array of all the property names of an object. 

For example, if an object called `person` has a property called `name`, it could be accessed in the following way:

```javascript
var keys = Object.keys(person);
var nameIndex = keys.indexOf("name");
var name = person[keys[nameIndex]];
```

## Object.getOwnPropertyNames()

A fourth way to access a variable property by name as a string in JavaScript is to use the `Object.getOwnPropertyNames()` method. This method returns an array of all the property names of an object, including non-enumerable properties. 

For example, if an object called `person` has a property called `name`, it could be accessed in the following way:

```javascript
var keys = Object.getOwnPropertyNames(person);
var nameIndex = keys.indexOf("name");
var name = person[keys[nameIndex]];
```
