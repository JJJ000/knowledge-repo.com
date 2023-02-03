---
title: Determine if a variable is a function type
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-03 00:00:00
updated_at: 2023-02-03 00:00:00
tldr: You can check if a variable is of function type in Javascript by using the typeof operator and checking if it returns `function`.
---

**Contents**

[TOC]

**Answer:**

**Using typeof Operator:**

The typeof operator is used to check the type of a variable in JavaScript. It returns a string with the type of the variable. If the variable is a function, it will return “function”.

Example:

```javascript
function func() {
  // some code
}

console.log(typeof func); // Output: function
```

**Using instanceof Operator:**

The instanceof operator is used to check whether an object is an instance of a particular constructor or not. If the variable is a function, it will return true.

Example:

```javascript
function func() {
  // some code
}

console.log(func instanceof Function); // Output: true
```

**Using Object.prototype.toString():**

The Object.prototype.toString() method is used to check the type of an object. If the variable is a function, it will return [object Function].

Example:

```javascript
function func() {
  // some code
}

console.log(Object.prototype.toString.call(func)); // Output: [object Function]
```
