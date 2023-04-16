---
title: What is the syntax for determining if a variable is an array in javascript?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: You can check if a variable is an array in JavaScript by using the Array.isArray() method.
---

**Contents**

[TOC]

## Using the Array.isArray() Method
The `Array.isArray()` method can be used to determine whether a variable is an array or not. This method returns a boolean value of `true` if the variable is an array, and `false` if it is not. 

Syntax:
```
Array.isArray(variable)
```

Example:
```
let fruits = ["apple", "banana", "mango"];
console.log(Array.isArray(fruits));
// Output: true
```

## Using the typeof Operator 
The `typeof` operator can also be used to determine whether a variable is an array or not. This method returns the string `"object"` if the variable is an array, and a different string (such as `"string"` or `"number"`) if it is not. 

Syntax:
```
typeof variable
```

Example:
```
let fruits = ["apple", "banana", "mango"];
console.log(typeof fruits);
// Output: object
```

## Using the instanceof Operator
The `instanceof` operator can also be used to determine whether a variable is an array or not. This method returns a boolean value of `true` if the variable is an array, and `false` if it is not. 

Syntax:
```
variable instanceof Array
```

Example:
```
let fruits = ["apple", "banana", "mango"];
console.log(fruits instanceof Array);
// Output: true
```
