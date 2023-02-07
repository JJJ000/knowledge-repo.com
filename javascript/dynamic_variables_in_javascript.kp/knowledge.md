---
title: Create variables with changing names in javascript
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: Dynamic variable names can be created by using the `let` keyword to declare variables that can be reassigned during runtime.
---

**Contents**

[TOC]

### Using Bracket Notation

Dynamic variable names can be used in JavaScript by using bracket notation. Bracket notation allows us to use variables to access properties of an object. For example:

```javascript
const myObject = {
  key1: 'value1',
  key2: 'value2'
};

const myKey = 'key1';

console.log(myObject[myKey]); // Output: 'value1'
```

In the above example, we have declared an object with two key-value pairs, and a variable `myKey` which holds the value of `key1`. We can then use `myObject[myKey]` to access the value of `key1` in the object.

### Using eval()

Dynamic variable names can also be used in JavaScript by using the `eval()` method. The `eval()` method parses a string as JavaScript code and executes it. For example:

```javascript
const myVariable = 'myValue';

eval('var ' + myVariable + ' = "Hello World";');

console.log(myValue); // Output: 'Hello World'
```

In the above example, we have declared a variable `myVariable` which holds the value of `myValue`. We can then use `eval('var ' + myVariable + ' = "Hello World";')` to create a new variable with the name `myValue` and assign it the value of `Hello World`.

### Using window Object

Dynamic variable names can also be used in JavaScript by using the `window` object. The `window` object is the global object in JavaScript and it provides access to all global variables and functions. For example:

```javascript
const myVariable = 'myValue';

window[myVariable] = 'Hello World';

console.log(myValue); // Output: 'Hello World'
```

In the above example, we have declared a variable `myVariable` which holds the value of `myValue`. We can then use `window[myVariable] = 'Hello World'` to create a new global variable with the name `myValue` and assign it the value of `Hello World`.
