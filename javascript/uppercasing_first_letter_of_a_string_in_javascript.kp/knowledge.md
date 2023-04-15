---
title: What is the syntax for capitalizing the first letter of a string in javascript?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-04-17 00:00:00
updated_at: 2023-04-17 00:00:00
tldr: Use the String.prototype.charAt() method with the String.prototype.toUpperCase() method to make the first letter of a string uppercase in JavaScript.
---

**Contents**

[TOC]

**Using the toUpperCase() Method**

1. Create a variable to store the string.

```javascript
let str = "hello world";
```

2. Use the `toUpperCase()` method on the string variable.

```javascript
let strUpper = str.toUpperCase();
```

3. Access the first character of the string using the `charAt()` method.

```javascript
let firstChar = strUpper.charAt(0);
```

4. Output the result.

```javascript
console.log(firstChar); // Outputs "H"
```

**Using Substring and toUpperCase()**

1. Create a variable to store the string.

```javascript
let str = "hello world";
```

2. Use the `substring()` method to extract the first character of the string.

```javascript
let firstChar = str.substring(0,1);
```

3. Use the `toUpperCase()` method on the first character.

```javascript
let firstCharUpper = firstChar.toUpperCase();
```

4. Output the result.

```javascript
console.log(firstCharUpper); // Outputs "H"
```
