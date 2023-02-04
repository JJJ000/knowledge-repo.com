---
title: What is the first character of a string?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-04 00:00:00
updated_at: 2023-02-04 00:00:00
tldr: Use the charAt() method to get the first character of a string in Javascript.
---

**Contents**

[TOC]

# Using Substring

The substring() method extracts the characters from a string, between two specified indices, and returns the new sub string.

Syntax:
```
string.substring(indexStart, indexEnd)
```

Example:
```
var str = "Hello World!";
var firstChar = str.substring(0,1);

console.log(firstChar); // Outputs "H"
```

# Using charAt()

The charAt() method returns the character at the specified index in a string.

Syntax:
```
string.charAt(index)
```

Example:
```
var str = "Hello World!";
var firstChar = str.charAt(0);

console.log(firstChar); // Outputs "H"
```

# Using Bracket Notation

The bracket notation allows you to access the character at a specified index.

Syntax:
```
string[index]
```

Example:
```
var str = "Hello World!";
var firstChar = str[0];

console.log(firstChar); // Outputs "H"
```

# Using Slice

The slice() method extracts a section of a string and returns a new string.

Syntax:
```
string.slice(startIndex, endIndex)
```

Example:
```
var str = "Hello World!";
var firstChar = str.slice(0,1);

console.log(firstChar); // Outputs "H"
```
