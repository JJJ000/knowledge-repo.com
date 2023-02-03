---
title: What is the syntax for removing spaces from a string in javascript?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-03 00:00:00
updated_at: 2023-02-03 00:00:00
tldr: Use the String.prototype.replace() method to replace spaces with an empty string.
---

**Contents**

[TOC]

#1 Using the Replace Method

The `replace()` method can be used to remove all spaces from a string. This method takes two parameters: the substring to be replaced and the substring to replace it with. To remove all spaces from a string, you can pass an empty string as the second parameter.

```javascript
let str = "Hello World";
let newStr = str.replace(/\s/g, "");
console.log(newStr); // Output: "HelloWorld"
```

#2 Using the Split and Join Methods

The `split()` and `join()` methods can also be used to remove all spaces from a string. This method takes a single parameter, which is the separator to split the string. To remove all spaces from a string, you can pass an empty string as the separator. The `join()` method takes the output of the `split()` method and joins it back together using the separator passed as the parameter.

```javascript
let str = "Hello World";
let newStr = str.split("").join("");
console.log(newStr); // Output: "HelloWorld"
```

#3 Using the Trim Method

The `trim()` method can be used to remove all leading and trailing spaces from a string. This method does not take any parameters and will remove all whitespace from the beginning and end of the string.

```javascript
let str = "  Hello World  ";
let newStr = str.trim();
console.log(newStr); // Output: "Hello World"
```

#4 Using Regular Expressions

Regular expressions can also be used to remove all spaces from a string. This method takes a single parameter, which is the regular expression to be used to match the spaces. To remove all spaces from a string, you can pass `/\s/g` as the parameter.

```javascript
let str = "Hello World";
let newStr = str.replace(/\s/g, "");
console.log(newStr); // Output: "HelloWorld"
```
