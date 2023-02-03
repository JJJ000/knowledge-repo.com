---
title: Change JavaScript string to lowercase
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-03 00:00:00
updated_at: 2023-02-03 00:00:00
tldr: The string can be converted to all lowercase by using the .toLowerCase() method.
---

**Contents**

[TOC]

1. Using `.toLowerCase()`
--------------------------------
The `.toLowerCase()` method can be used to convert a string to all lowercase characters. 

```javascript
let originalString = "Hello World!";
let lowercaseString = originalString.toLowerCase();

console.log(lowercaseString); // Outputs "hello world!"
```

2. Using `String.prototype.replace()`
------------------------------------
The `String.prototype.replace()` method can be used to convert a string to all lowercase characters. 

```javascript
let originalString = "Hello World!";
let lowercaseString = originalString.replace(/[A-Z]/g, char => char.toLowerCase());

console.log(lowercaseString); // Outputs "hello world!"
```

3. Using `String.prototype.split()`
----------------------------------
The `String.prototype.split()` method can be used to convert a string to all lowercase characters. 

```javascript
let originalString = "Hello World!";
let lowercaseString = originalString.split('').map(char => char.toLowerCase()).join('');

console.log(lowercaseString); // Outputs "hello world!"
```

4. Using a `for` Loop
---------------------
A `for` loop can be used to convert a string to all lowercase characters. 

```javascript
let originalString = "Hello World!";
let lowercaseString = '';

for (let i = 0; i < originalString.length; i++) {
    lowercaseString += originalString[i].toLowerCase();
}

console.log(lowercaseString); // Outputs "hello world!"
```
