---
title: What is the syntax for determining if a string includes a specific character in javascript?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: Use the String.prototype.includes() method to check if a string contains a certain character.
---

**Contents**

[TOC]

**Using includes() Method**

The includes() method checks whether a string contains the specified character or not, and returns a boolean value.

Syntax: 
```javascript
string.includes(character)
```

Example:
```javascript
let str = "Hello World!";
let character = "W";

console.log(str.includes(character));
// Output: true
```

**Using indexOf() Method**

The indexOf() method returns the index of the specified character in the string, and returns -1 if the character is not found.

Syntax: 
```javascript
string.indexOf(character)
```

Example:
```javascript
let str = "Hello World!";
let character = "W";

console.log(str.indexOf(character));
// Output: 6
```

**Using regex Method**

The regex method searches for a pattern in the string and returns true if the pattern is found, and false if not.

Syntax: 
```javascript
/pattern/.test(string)
```

Example:
```javascript
let str = "Hello World!";
let character = "W";

console.log(/W/.test(str));
// Output: true
```
