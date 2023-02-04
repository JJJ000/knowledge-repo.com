---
title: How can I limit a string to its first n characters?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-04 00:00:00
updated_at: 2023-02-04 00:00:00
tldr: Use the substring() method to keep only the first n characters in a string.
---

**Contents**

[TOC]

**Section 1: Using Substring**

To keep only the first `n` characters in a string, you can use the substring method. 

Syntax:
```
string.substring(0, n);
```

where `n` is the number of characters you want to keep.

**Section 2: Example**

For example, if you have the string `"Hello World"` and you want to keep only the first 5 characters, you can use the following code:

```
let str = "Hello World";
let newStr = str.substring(0, 5);
console.log(newStr); // Outputs "Hello"
```

**Section 3: Limitations**

The substring method has some limitations. For example, it can only be used to extract a portion of a string, and it does not work with negative values. 

**Section 4: Alternative**

An alternative to using the substring method is to use the slice method. The syntax for this method is similar to that of the substring method, but it has the added advantage of being able to accept negative values.
