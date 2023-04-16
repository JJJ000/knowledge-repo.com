---
title: How to replace all periods in a string using javascript
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Use the String.prototype.replace() method to replace all dots in a string with a specified value.
---

**Contents**

[TOC]

## Method 1: Using Regular Expressions

```javascript
let string = "This is a string with a lot of dots....";
let newString = string.replace(/\./g, "");
console.log(newString); //This is a string with a lot of dots
```

## Method 2: Using String.prototype.replace()

```javascript
let string = "This is a string with a lot of dots....";
let newString = string.replace(/\./g, "");
console.log(newString); //This is a string with a lot of dots
```

## Method 3: Using a For Loop

```javascript
let string = "This is a string with a lot of dots....";
let newString = "";
for (let i = 0; i < string.length; i++) {
  if (string[i] !== ".") {
    newString += string[i];
  }
}
console.log(newString); //This is a string with a lot of dots
```

## Method 4: Using Array.prototype.map()

```javascript
let string = "This is a string with a lot of dots....";
let newString = string
  .split("")
  .map(char => (char === "." ? "" : char))
  .join("");
console.log(newString); //This is a string with a lot of dots
```
