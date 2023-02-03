---
title: Eliminate all blank spaces from text
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-03 00:00:00
updated_at: 2023-02-03 00:00:00
tldr: Use the String.prototype.replace() method to replace all white spaces with an empty string.
---

**Contents**

[TOC]

**Using Regular Expressions**

```javascript
let str = "This is a string with white spaces";

let newStr = str.replace(/\s/g, "");

console.log(newStr); // Output: "Thisisastringwithwhitespaces"
```

**Using String.prototype.replace()**

```javascript
let str = "This is a string with white spaces";

let newStr = str.replace(/\s/g, "");

console.log(newStr); // Output: "Thisisastringwithwhitespaces"
```

**Using String.prototype.split() and Array.prototype.join()**

```javascript
let str = "This is a string with white spaces";

let newStr = str.split(" ").join("");

console.log(newStr); // Output: "Thisisastringwithwhitespaces"
```

**Using a For Loop**

```javascript
let str = "This is a string with white spaces";
let newStr = "";

for (let i = 0; i < str.length; i++) {
  if (str[i] !== " ") {
    newStr += str[i];
  }
}

console.log(newStr); // Output: "Thisisastringwithwhitespaces"
```
