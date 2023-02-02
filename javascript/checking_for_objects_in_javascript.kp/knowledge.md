---
title: Determine if a value is an object in javascript
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-02 00:00:00
updated_at: 2023-02-02 00:00:00
tldr: You can use the typeof operator to check if a value is an object in JavaScript.
---

**Contents**

[TOC]

## Using typeof Operator 
We can use the `typeof` operator to check if a value is an object in JavaScript. The `typeof` operator returns a string indicating the type of the unevaluated operand. 

Syntax: 
`typeof operand`

Example: 

```
let obj = {name: "John"};

console.log(typeof obj); // Output: object
```

## Using instanceof Operator 
We can also use the `instanceof` operator to check if a value is an object in JavaScript. The `instanceof` operator returns `true` if the specified object is an instance of the specified object. 

Syntax: 
`object instanceof constructor`

Example: 

```
let obj = {name: "John"};

console.log(obj instanceof Object); // Output: true
```

## Using Object.prototype.toString.call() 
We can also use the `Object.prototype.toString.call()` method to check if a value is an object in JavaScript. This method returns a string representing the object's class.

Syntax: 
`Object.prototype.toString.call(object)`

Example: 

```
let obj = {name: "John"};

console.log(Object.prototype.toString.call(obj)); // Output: [object Object]
```
