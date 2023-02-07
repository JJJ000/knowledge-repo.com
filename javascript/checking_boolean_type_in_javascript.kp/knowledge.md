---
title: What is the process for determining if a data type is boolean?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: You can check if a type is Boolean in Javascript by using the typeof operator.
---

**Contents**

[TOC]

1. Using the `typeof` Operator 

The `typeof` operator can be used to check if a value is a boolean. The `typeof` operator returns a string with the type of the given value. 

```
let boolVal = true;

console.log(typeof boolVal); // Output: boolean
```

2. Using the `instanceof` Operator 

The `instanceof` operator can be used to check if an object is an instance of a particular constructor. This operator works for primitive values as well. 

```
let boolVal = true;

console.log(boolVal instanceof Boolean); // Output: true
```

3. Using the `Object.prototype.toString()` Method 

The `Object.prototype.toString()` method can be used to get the string representation of an object's type. 

```
let boolVal = true;

console.log(Object.prototype.toString.call(boolVal)); // Output: [object Boolean]
```

4. Using the `Object.prototype.constructor` Property 

The `Object.prototype.constructor` property returns the constructor function for an object. This can be used to check if the object is of a particular type. 

```
let boolVal = true;

console.log(boolVal.constructor === Boolean); // Output: true
```
