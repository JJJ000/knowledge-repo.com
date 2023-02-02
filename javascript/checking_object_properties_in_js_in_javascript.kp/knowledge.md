---
title: What is the procedure for determining if an object has a particular property in javascript?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-02 00:00:00
updated_at: 2023-02-02 00:00:00
tldr: You can use the `in` operator to check if an object has a specific property in JavaScript.
---

**Contents**

[TOC]

## Using the `in` operator

The `in` operator can be used to check if an object has a specific property.

Syntax:
```
propertyName in objectName
```

Example:
```
let person = {
  name: 'John',
  age: 25
};

console.log('name' in person);  // Output: true
console.log('height' in person);  // Output: false
```

## Using the `hasOwnProperty()` method

The `hasOwnProperty()` method can be used to check if an object has a specific property.

Syntax:
```
objectName.hasOwnProperty(propertyName)
```

Example:
```
let person = {
  name: 'John',
  age: 25
};

console.log(person.hasOwnProperty('name'));  // Output: true
console.log(person.hasOwnProperty('height'));  // Output: false
```
