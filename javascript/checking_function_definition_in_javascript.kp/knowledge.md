---
title: What are the signs that a JavaScript function has been declared?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: You can check if a JavaScript function is defined by using the typeof operator to check if the function is equal to `function`.
---

**Contents**

[TOC]

# Section 1: Check the Function's Name

One way to check if a JavaScript function is defined is to check the name of the function.  If the function has been defined, then its name will be defined in the global scope. To check for this, you can use the `typeof` operator. The `typeof` operator will return a string representing the type of the given variable. If the function has been defined, then `typeof` will return `"function"`. 

For example: 

```javascript
let myFunction = () => {
    // do something
}

console.log(typeof myFunction); // "function"
```

# Section 2: Check the Function's Definition

Another way to check if a JavaScript function is defined is to check its definition. This can be done by calling the `toString` method on the function. This will return a string representing the function's definition. If the function has been defined, the definition will be returned.

For example: 

```javascript
let myFunction = () => {
    // do something
}

console.log(myFunction.toString()); // "() => { // do something }"
```

# Section 3: Try to Call the Function

The last way to check if a JavaScript function is defined is to try to call the function. If the function has been defined, then it can be called without any errors. If the function has not been defined, then calling it will throw an error.

For example:

```javascript
let myFunction = () => {
    // do something
}

myFunction(); // No error

myUndefinedFunction(); // Error: myUndefinedFunction is not defined
```

# Section 4: Use the Function's Prototype

Another way to check if a JavaScript function is defined is to check its prototype. If the function has been defined, then its prototype will be available. To check for this, you can use the `hasOwnProperty` method on the function's prototype. This will return a boolean indicating whether the given property is defined on the prototype or not.

For example:

```javascript
let myFunction = () => {
    // do something
}

console.log(myFunction.prototype.hasOwnProperty("toString")); // true
```
