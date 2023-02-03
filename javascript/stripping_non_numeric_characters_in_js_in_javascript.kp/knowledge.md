---
title: Remove all non-numeric characters from a string in javascript
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-03 00:00:00
updated_at: 2023-02-03 00:00:00
tldr: Use the replace() method to replace all non-numeric characters with an empty string.
---

**Contents**

[TOC]

**Using Regular Expressions:**

```javascript
let str = "Hello123World456";
let newStr = str.replace(/\D/g, '');
console.log(newStr); // 123456
```

**Using Loops:**

```javascript
let str = "Hello123World456";
let newStr = '';
for (let i = 0; i < str.length; i++) {
  if (str[i] >= '0' && str[i] <= '9') {
    newStr += str[i];
  }
}
console.log(newStr); // 123456
```

**Using Array.prototype.filter():**

```javascript
let str = "Hello123World456";
let newStr = str.split('').filter(char => char >= '0' && char <= '9').join('');
console.log(newStr); // 123456
```

**Using Array.prototype.reduce():**

```javascript
let str = "Hello123World456";
let newStr = str.split('').reduce((acc, char) => char >= '0' && char <= '9' ? acc + char : acc, '');
console.log(newStr); // 123456
```
