---
title: Regular expression to determine if a string consists solely of numbers
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: The regex to check whether a string contains only numbers is \d+
---

**Contents**

[TOC]

### 1. Regex
`^[0-9]+$`

### 2. Explanation
The regex `^[0-9]+$` checks for strings that contain only numbers. The `^` symbol denotes the start of the string, and the `$` symbol denotes the end of the string. The `[0-9]` character class matches any single digit from 0 to 9, and the `+` symbol denotes one or more of the preceding character.

### 3. Usage
This regex can be used to check if a string contains only numbers by passing the string to a regular expression matching function, such as `RegExp.test()` in Javascript.

### 4. Example
```javascript
let regex = /^[0-9]+$/;
let str = "12345";

console.log(regex.test(str)); //true
```
