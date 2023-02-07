---
title: What is the name of the JavaScript function that adds characters to the end of a string to make it reach a specific length?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: Yes, the built-in String.prototype.padStart() and String.prototype.padEnd() functions can be used to pad a string to a determined length.
---

**Contents**

[TOC]

## String.prototype.padStart()

The `String.prototype.padStart()` method pads the current string with another string (multiple times, if needed) until the resulting string reaches the given length. The padding is applied from the start of the current string.

## Syntax

```
str.padStart(targetLength [, padString])
```

## Parameters

**targetLength**

The length of the resulting string once the current string has been padded. If the value of **targetLength** is less than the length of the current string, the current string will be returned as is.

**padString**

Optional. The string to pad the current string with. If this string is too long, it will be truncated and the remaining characters will be used to pad the string. The default value is " " (U+0020).

## Examples

```
let str1 = 'Bread'
console.log(str1.padStart(10)); // "    Bread"
console.log(str1.padStart(10, "*")); // "****Bread"
console.log(str1.padStart(6, "12345")); // "123Bread"
console.log(str1.padStart(1)); // "Bread"
```
