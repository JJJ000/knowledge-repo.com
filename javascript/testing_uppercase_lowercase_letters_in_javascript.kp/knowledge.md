---
title: What is the best way to determine if a particular letter in a string is in upper or lower case using javascript?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: You can use the String.prototype.toUpperCase() or String.prototype.toLowerCase() functions to compare the original string to the converted string and determine if the letter is uppercase or lowercase.
---

**Contents**

[TOC]

## Using Regular Expressions

Regular expressions provide a way to test whether a letter in a string is uppercase or lowercase. The following code can be used to test if a letter is uppercase or lowercase:

```javascript
let str = "Hello World";
let regex = /[A-Z]/;
let isUpperCase = regex.test(str);
if (isUpperCase) {
  console.log("The letter is uppercase");
} else {
  console.log("The letter is lowercase");
}
```

## Using toUpperCase() and toLowerCase()

The `toUpperCase()` and `toLowerCase()` methods can be used to convert a letter in a string to uppercase or lowercase. The following code can be used to test if a letter is uppercase or lowercase:

```javascript
let str = "Hello World";
let upperCaseStr = str.toUpperCase();
let lowerCaseStr = str.toLowerCase();
if (str === upperCaseStr) {
  console.log("The letter is uppercase");
} else if (str === lowerCaseStr) {
  console.log("The letter is lowercase");
}
```

## Using Character Codes

The `charCodeAt()` method can be used to get the character code of a letter in a string. The character code for uppercase letters is between 65 and 90, and the character code for lowercase letters is between 97 and 122. The following code can be used to test if a letter is uppercase or lowercase:

```javascript
let str = "Hello World";
let charCode = str.charCodeAt(0);
if (charCode >= 65 && charCode <= 90) {
  console.log("The letter is uppercase");
} else if (charCode >= 97 && charCode <= 122) {
  console.log("The letter is lowercase");
}
```
