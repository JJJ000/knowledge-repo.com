---
title: What is the best way to get a numerical value from a string in javascript?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Use the String.match() method to extract a number from a string.
---

**Contents**

[TOC]

### Using Regular Expressions

Regular expressions can be used to extract a number from a string. To do this, you can use the `RegExp` constructor to create a regular expression object and then use the `exec()` method to match the pattern and extract the number.

Example:

```js
let str = "The number is 42";

let regex = new RegExp('\\d+');
let result = regex.exec(str);

console.log(result[0]); // 42
```

### Using String Methods

You can also use string methods such as `match()` or `search()` to extract a number from a string.

Example:

```js
let str = "The number is 42";

let result = str.match(/\d+/);

console.log(result[0]); // 42
```

### Using Array Methods

You can also use array methods such as `map()` or `filter()` to extract a number from a string.

Example:

```js
let str = "The number is 42";

let result = str.split(' ').map(Number).filter(n => !isNaN(n));

console.log(result[0]); // 42
```

### Using Math Functions

You can also use math functions such as `parseInt()` or `parseFloat()` to extract a number from a string.

Example:

```js
let str = "The number is 42";

let result = parseInt(str.match(/\d+/)[0]);

console.log(result); // 42
```
