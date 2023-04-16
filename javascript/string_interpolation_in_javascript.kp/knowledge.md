---
title: What is the process for inserting values into a string using javascript?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: String interpolation in JavaScript can be done using template literals, which are denoted by backticks (`).
---

**Contents**

[TOC]

## Using Template Literals
Template literals are string literals that allow embedded expressions. Template literals use back-tick (`) characters instead of single or double quotation marks.

Syntax:
```javascript
let myName = 'John';
console.log(`My name is ${myName}`); 
// Output: My name is John
```

## Using String.replace()
The String.replace() method can be used to replace part of a string with another string.

Syntax:
```javascript
let myName = 'John';
let myString = 'My name is %name%';
let newString = myString.replace('%name%', myName);
console.log(newString); 
// Output: My name is John
```

## Using String Concatenation
String concatenation is the process of combining two or more strings together.

Syntax:
```javascript
let myName = 'John';
let myString = 'My name is ' + myName;
console.log(myString); 
// Output: My name is John
```
