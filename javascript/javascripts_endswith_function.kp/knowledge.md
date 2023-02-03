---
title: Javascript's 'endswith' function
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-03 00:00:00
updated_at: 2023-02-03 00:00:00
tldr: The endsWith() method checks whether a string ends with the specified string/characters.
---

**Contents**

[TOC]

# Syntax

The syntax for the String.prototype.endsWith() method is as follows:

```
str.endsWith(searchString[, length])
```

# Parameters

**searchString**

A string to be searched for at the end of the given string.

**length**

Optional. An integer specifying the number of characters to be considered for the search. If omitted, the length of the given string is used.

# Return Value

A Boolean indicating whether or not the given string ends with the specified search string.

# Examples

```
let str = 'To be, or not to be, that is the question.';

console.log(str.endsWith('question.')); // true
console.log(str.endsWith('to be')); // false
console.log(str.endsWith('to be', 19)); // true
```
