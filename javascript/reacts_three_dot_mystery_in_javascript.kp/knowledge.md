---
title: What is the purpose of the three dots (...) in react?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-03 00:00:00
updated_at: 2023-02-03 00:00:00
tldr: The three dots in React are used to spread an array of values into individual values.
---

**Contents**

[TOC]

#### Spread Operator
The three dots in React are known as the spread operator. This operator allows an expression to be expanded in places where multiple arguments (for function calls) or multiple elements (for array literals) are expected. It can also be used to expand an object's properties.

#### Syntax
The syntax for the spread operator is three dots (...) followed by the array or object that needs to be expanded. 

#### Examples
Here is an example of the spread operator being used in a function call:

```javascript
const numbers = [1, 2, 3];

Math.max(...numbers); // returns 3
```

Here is an example of the spread operator being used to expand an object's properties:

```javascript
const person = {
  name: 'John',
  age: 21
};

const newPerson = {
  ...person,
  gender: 'male'
};

console.log(newPerson); // {name: 'John', age: 21, gender: 'male'}
```
