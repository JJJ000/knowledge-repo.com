---
title: What is the best way to explain "object" parameters in jsdoc?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-04 00:00:00
updated_at: 2023-02-04 00:00:00
tldr: In JSDoc, an `object` argument is a parameter that is an object containing properties and values.
---

**Contents**

[TOC]

# Definition
Object arguments are arguments that are passed to a function in the form of a JavaScript object. Object arguments allow for the passing of multiple values to a function in a single argument.

# Syntax
Object arguments are written in the following syntax:

```javascript
functionName( { key1: value1, key2: value2, ... } );
```

# Examples
Object arguments can be used to pass multiple values to a function in a single argument. For example, the following code passes two values to a function using an object argument:

```javascript
function greetUser(options) {
  console.log(`Hello, ${options.name}! You are ${options.age} years old.`);
}

greetUser({ name: 'John', age: 30 });
// Output: Hello, John! You are 30 years old.
```

# JSDoc
Object arguments should be documented using the `@param` tag and the `{Object}` type. For example:

```javascript
/**
 * Greets a user
 * 
 * @param {Object} options The options object
 * @param {string} options.name The user's name
 * @param {number} options.age The user's age
 */
function greetUser(options) {
  // ...
}
```
