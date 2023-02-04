---
title: What is the method for converting a string into an array of characters?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-04 00:00:00
updated_at: 2023-02-04 00:00:00
tldr: Use the split() method to get an array of characters from a string in Javascript.
---

**Contents**

[TOC]

# Section 1: Using the split() Method
The `split()` method can be used to convert a string into a character array. This method takes a single argument, which is a separator used to identify where to split the string.

For example, the following code will split the string `"Hello World"` into an array of characters:

```javascript
var str = "Hello World";
var charArray = str.split("");
console.log(charArray); // ["H", "e", "l", "l", "o", " ", "W", "o", "r", "l", "d"]
```

# Section 2: Using the for loop
The `for` loop can also be used to convert a string into a character array. This method takes no arguments and iterates over each character in the string, adding each character to an array.

For example, the following code will split the string `"Hello World"` into an array of characters:

```javascript
var str = "Hello World";
var charArray = [];
for (var i = 0; i < str.length; i++) {
  charArray.push(str[i]);
}
console.log(charArray); // ["H", "e", "l", "l", "o", " ", "W", "o", "r", "l", "d"]
```

# Section 3: Using the spread operator
The spread operator (`...`) can also be used to convert a string into a character array. This method takes no arguments and iterates over each character in the string, adding each character to an array.

For example, the following code will split the string `"Hello World"` into an array of characters:

```javascript
var str = "Hello World";
var charArray = [...str];
console.log(charArray); // ["H", "e", "l", "l", "o", " ", "W", "o", "r", "l", "d"]
```

# Section 4: Using the Array.from() Method
The `Array.from()` method can also be used to convert a string into a character array. This method takes a single argument, which is the string to be converted.

For example, the following code will split the string `"Hello World"` into an array of characters:

```javascript
var str = "Hello World";
var charArray = Array.from(str);
console.log(charArray); // ["H", "e", "l", "l", "o", " ", "W", "o", "r", "l", "d"]
```
