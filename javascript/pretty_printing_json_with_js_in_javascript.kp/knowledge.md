---
title: Print JSON in a readable format using javascript
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-04-17 00:00:00
updated_at: 2023-04-17 00:00:00
tldr: Using the built-in JSON.stringify() method, you can pretty-print JSON in JavaScript.
---

**Contents**

[TOC]

### Method 1: Using JSON.stringify

The `JSON.stringify()` method is used to convert a JavaScript object or value to a JSON string. It takes two parameters: the value to be converted and an optional replacer function.

Syntax:

```
JSON.stringify(value[, replacer[, space]])
```

Example:

```js
var person = {
  name: "John Doe",
  age: 25
};

var prettyPerson = JSON.stringify(person, null, 2);

console.log(prettyPerson);

// Output:
// {
//   "name": "John Doe",
//   "age": 25
// }
```

### Method 2: Using a Third-Party Library

There are several third-party libraries available for formatting JSON. One of the most popular is the `json-formatter-js` library.

Example:

```js
const JSONFormatter = require('json-formatter-js');

var person = {
  name: "John Doe",
  age: 25
};

var formatter = new JSONFormatter(person, 2);

console.log(formatter.render());

// Output:
// {
//   "name": "John Doe",
//   "age": 25
// }
```
