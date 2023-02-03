---
title: Verify if a string conforms to a regular expression in javascript
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-03 00:00:00
updated_at: 2023-02-03 00:00:00
tldr: You can use the RegExp.prototype.test() method to check if a string matches a regex in Javascript.
---

**Contents**

[TOC]

### Using Regular Expressions

The easiest way to check if a string matches a regular expression is to use the `test()` method. This method takes a regular expression as an argument and returns `true` if the string matches the pattern, and `false` if it doesn't.

For example:

```javascript
let regex = /^[a-zA-Z]+$/;
let string = "HelloWorld";

let result = regex.test(string);

console.log(result); // false
```

### Using String.match()

Another way to check if a string matches a regular expression is to use the `match()` method. This method takes a regular expression as an argument and returns an array of matches if the string matches the pattern, and `null` if it doesn't.

For example:

```javascript
let regex = /^[a-zA-Z]+$/;
let string = "HelloWorld";

let result = string.match(regex);

console.log(result); // null
```

### Using String.search()

The `search()` method is similar to the `match()` method in that it takes a regular expression as an argument and returns an integer indicating the position of the first match if the string matches the pattern, and `-1` if it doesn't.

For example:

```javascript
let regex = /^[a-zA-Z]+$/;
let string = "HelloWorld";

let result = string.search(regex);

console.log(result); // -1
```

### Using String.includes()

The `includes()` method is another way to check if a string matches a regular expression. This method takes a regular expression as an argument and returns `true` if the string matches the pattern, and `false` if it doesn't.

For example:

```javascript
let regex = /^[a-zA-Z]+$/;
let string = "HelloWorld";

let result = string.includes(regex);

console.log(result); // false
```
