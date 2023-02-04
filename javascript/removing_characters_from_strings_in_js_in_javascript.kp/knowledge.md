---
title: What is the best way to delete a character from a string using javascript?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-04 00:00:00
updated_at: 2023-02-04 00:00:00
tldr: You can use the String.prototype.replace() method to remove a character from a string in JavaScript.
---

**Contents**

[TOC]

1. Using String.prototype.replace()

String.prototype.replace() is a method used to replace a character in a string with a given character or string. It takes two parameters:

- The first parameter is a regular expression which is used to match the character to be replaced.
- The second parameter is the replacement character or string.

```
let string = 'Hello World';
let newString = string.replace(/o/, '');

console.log(newString); // 'Hell World'
```

2. Using String.prototype.split()

String.prototype.split() is a method used to split a string into an array of strings. It takes one parameter which is a regular expression which is used to match the character to be removed.

```
let string = 'Hello World';
let newString = string.split(/o/)[0] + string.split(/o/)[1];

console.log(newString); // 'Hell World'
```

3. Using String.prototype.slice()

String.prototype.slice() is a method used to return a part of a string. It takes two parameters:

- The first parameter is the starting index of the part to be returned.
- The second parameter is the end index of the part to be returned.

```
let string = 'Hello World';
let newString = string.slice(0,4) + string.slice(5);

console.log(newString); // 'Hell World'
```

4. Using String.prototype.substring()

String.prototype.substring() is a method used to return a part of a string. It takes two parameters:

- The first parameter is the starting index of the part to be returned.
- The second parameter is the end index of the part to be returned.

```
let string = 'Hello World';
let newString = string.substring(0,4) + string.substring(5);

console.log(newString); // 'Hell World'
```
