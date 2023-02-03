---
title: Assign a value to an object's property using a variable in javascript
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-02 00:00:00
updated_at: 2023-02-02 00:00:00
tldr: You can set an object key by a variable in JavaScript by using bracket notation and assigning the variable to the key.
---

**Contents**

[TOC]

### Using Bracket Notation

We can use bracket notation to set an object key by a variable. This is done by using the variable name as a string inside the brackets.

```javascript
let key = 'name';
let person = {};

person[key] = 'John';

console.log(person); // { name: 'John' }
```

### Using Object.defineProperty

We can also use `Object.defineProperty()` to set an object key by a variable. This is done by passing the variable name as the first argument of the method.

```javascript
let key = 'name';
let person = {};

Object.defineProperty(person, key, {
  value: 'John',
  writable: true,
  enumerable: true,
  configurable: true
});

console.log(person); // { name: 'John' }
```

### Using Object.assign

We can use `Object.assign()` to set an object key by a variable. This is done by passing the variable name as the key of the source object.

```javascript
let key = 'name';
let person = {};

Object.assign(person, { [key]: 'John' });

console.log(person); // { name: 'John' }
```

### Using Spread Syntax

We can also use the spread syntax to set an object key by a variable. This is done by passing the variable name as the key of the spreaded object.

```javascript
let key = 'name';
let person = {};

person = { ...person, [key]: 'John' };

console.log(person); // { name: 'John' }
```
