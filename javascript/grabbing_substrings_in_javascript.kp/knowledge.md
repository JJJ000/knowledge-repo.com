---
title: What is the syntax for extracting a substring before a specified character in javascript?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: Use the String.prototype.split() method to split the string into an array of substrings, then access the desired substring from the array.
---

**Contents**

[TOC]

# Using Substring

The `substring()` method can be used to grab a substring before a specified character in Javascript.

Syntax:
```
string.substring(start, end)
```

Example:
```
let str = "Hello World!";
let beforeCharacter = str.substring(0, str.indexOf("!"));
console.log(beforeCharacter);
// Output: "Hello World"
```

# Using Split

The `split()` method can also be used to grab a substring before a specified character in Javascript.

Syntax:
```
string.split(separator, limit)
```

Example:
```
let str = "Hello World!";
let beforeCharacter = str.split("!")[0];
console.log(beforeCharacter);
// Output: "Hello World"
```
