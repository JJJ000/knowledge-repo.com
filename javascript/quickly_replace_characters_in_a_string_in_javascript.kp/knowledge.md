---
title: Quickest way to replace all occurrences of a character in a string
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-03 00:00:00
updated_at: 2023-02-03 00:00:00
tldr: The fastest method to replace all instances of a character in a string in Javascript is to use the String.prototype.replace() method.
---

**Contents**

[TOC]

**1. Using the replace() Method:**

The replace() method is the simplest and most efficient way to replace a character in a string. It takes two parameters, the first being the character to be replaced, and the second being the character to replace it with.

Syntax: 

`string.replace(characterToReplace, replacementCharacter);`

Example:

`let str = "Hello World!";
str = str.replace("o", "a");
console.log(str); // Output: "Halla Warld!"`

**2. Using Regular Expressions:**

Regular expressions are powerful tools for matching patterns in strings. They can be used to replace all instances of a character in a string.

Syntax: 

`string.replace(/characterToReplace/g, replacementCharacter);`

Example:

`let str = "Hello World!";
str = str.replace(/o/g, "a");
console.log(str); // Output: "Halla Warld!"`

**3. Using a For Loop:**

A for loop can be used to iterate through a string and replace each instance of a character with a different character.

Syntax:

```
let str = "Hello World!";
let newStr = "";
for (let i = 0; i < str.length; i++) {
  if (str[i] === "o") {
    newStr += "a";
  } else {
    newStr += str[i];
  }
}
console.log(newStr); // Output: "Halla Warld!"
```

**4. Using Array.map():**

The Array.map() method can be used to iterate through a string and replace each instance of a character with a different character.

Syntax:

```
let str = "Hello World!";
let newStr = str.split("").map(char => {
  if (char === "o") {
    return "a";
  } else {
    return char;
  }
}).join("");
console.log(newStr); // Output: "Halla Warld!"
```
