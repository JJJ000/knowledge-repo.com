---
title: What is the best way to insert variables into strings in JavaScript without using string concatenation?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: You can use template literals (or `template strings`) to interpolate variables in strings in JavaScript without concatenation.
---

**Contents**

[TOC]

## Template Literals
Template literals are a new way of defining strings in JavaScript, introduced in ES6. Template literals use backtick (`) characters to define strings, and allow for the interpolation of variables using the ${} syntax. This allows for strings to be defined without the need for concatenation. 

## Syntax
Template literals are defined using backtick (`) characters, instead of single or double quotes. Inside the backticks, variables can be interpolated using the ${} syntax. Variables can also be evaluated using JavaScript expressions. 

## Example
Below is an example of a template literal, which interpolates a variable and evaluates an expression:

```javascript
let myName = 'John';
let myAge = 20;

let myString = `My name is ${myName} and I am ${myAge + 5} years old.`;

console.log(myString); // Outputs "My name is John and I am 25 years old."
```

## Advantages
Template literals offer a number of advantages over traditional string concatenation. They are easier to read, as they do not require the use of string concatenation operators. They also allow for the interpolation of variables and the evaluation of JavaScript expressions, making them more powerful and versatile.
