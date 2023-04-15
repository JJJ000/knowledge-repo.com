---
title: What is the best way to determine if a string contains a certain substring in javascript?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-04-17 00:00:00
updated_at: 2023-04-17 00:00:00
tldr: You can use the String.prototype.includes() method to check if a string contains a substring.
---

**Contents**

[TOC]

### Using the `includes()` Method

The `includes()` method can be used to check if a string contains a substring. This method returns a boolean value (`true` or `false`) depending on whether the substring is found in the string.

Syntax: 
`string.includes(substring)`

Example: 
```
let str = "Hello World";
let substring = "World";

console.log(str.includes(substring)); // Output: true
```

### Using the `indexOf()` Method

The `indexOf()` method can also be used to check if a string contains a substring. This method returns the index of the first occurrence of the substring in the string, or `-1` if the substring is not found.

Syntax: 
`string.indexOf(substring)`

Example: 
```
let str = "Hello World";
let substring = "World";

console.log(str.indexOf(substring)); // Output: 6
```

### Using the `search()` Method

The `search()` method is similar to the `indexOf()` method, but it is more powerful. It can accept a regular expression as an argument, which allows for more complex searches.

Syntax: 
`string.search(regexp)`

Example: 
```
let str = "Hello World";
let regexp = /world/i;

console.log(str.search(regexp)); // Output: 6
```

### Using the `match()` Method

The `match()` method can be used to check if a string contains a substring. This method returns an array of matches, or `null` if the substring is not found.

Syntax: 
`string.match(regexp)`

Example: 
```
let str = "Hello World";
let regexp = /world/i;

console.log(str.match(regexp)); // Output: ["World"]
```
