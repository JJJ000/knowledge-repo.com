---
title: Delete all characters after a certain point
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: Use the String.prototype.split() method, passing in the character as the argument, and then use the Array.prototype.shift() method to remove everything after the specified character.
---

**Contents**

[TOC]

**Section 1: Create a String**

Create a string that contains the character you want to remove everything after.

```javascript
let str = "This is a string with a ! in it!";
```

**Section 2: Find the Character Index**

Find the index of the character you want to remove everything after.

```javascript
let charIndex = str.indexOf("!");
```

**Section 3: Slice the String**

Slice the string up to the index of the character.

```javascript
let newStr = str.slice(0, charIndex);
```

**Section 4: Output the Result**

Output the result.

```javascript
console.log(newStr); // This is a string with a
```
