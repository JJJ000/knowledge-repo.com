---
title: What is the syntax for assigning a variable as a key in a JavaScript object literal?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-04 00:00:00
updated_at: 2023-02-04 00:00:00
tldr: You can use the variable as the key in the object literal by wrapping the variable in square brackets.
---

**Contents**

[TOC]

## Declaring the Variable

Variables can be declared in a JavaScript object literal by using the `let` keyword. For example,

```javascript
let myVariable = 'value';

let myObject = {
  [myVariable]: 'someValue'
};
```

## Accessing the Variable

The variable can be accessed in the object literal by using the `[]` syntax. For example,

```javascript
let myVariable = 'value';

let myObject = {
  [myVariable]: 'someValue'
};

console.log(myObject[myVariable]); // prints 'someValue'
```

## Updating the Variable

The variable can be updated in the object literal by using the `[]` syntax. For example,

```javascript
let myVariable = 'value';

let myObject = {
  [myVariable]: 'someValue'
};

myObject[myVariable] = 'newValue';

console.log(myObject[myVariable]); // prints 'newValue'
```

## Deleting the Variable

The variable can be deleted in the object literal by using the `delete` keyword. For example,

```javascript
let myVariable = 'value';

let myObject = {
  [myVariable]: 'someValue'
};

delete myObject[myVariable];

console.log(myObject[myVariable]); // prints 'undefined'
```
