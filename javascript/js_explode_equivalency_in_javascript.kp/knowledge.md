---
title: Javascript split() function
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: The Javascript equivalent to PHP`s explode() is the split() method.
---

**Contents**

[TOC]

**1. Array.prototype.split()**

The Array.prototype.split() method is the closest equivalent to the PHP explode() method. It is a built-in JavaScript function that splits a string into an array of substrings based on a separator. It takes two arguments: the string to be split, and the separator.

**2. Syntax**

The syntax for split() is as follows:

```
string.split(separator, limit)
```

The separator argument is required, and it defines the character, or the regular expression, to use for splitting the string. The limit argument is optional, and it defines the number of splits to be made.

**3. Example**

For example, to split a string by commas, the following code can be used:

```
let str = 'Hello,World,Foo,Bar';
let arr = str.split(',');

console.log(arr);  // ["Hello", "World", "Foo", "Bar"]
```

**4. Limitations**

The split() method has some limitations compared to the PHP explode() method. For example, the split() method does not support negative limit values, and it does not allow for the removal of empty strings from the resulting array.
