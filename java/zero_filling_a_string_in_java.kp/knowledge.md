---
title: Adding zeros to the beginning of a string
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: String.format(`%0` + desiredLength + `d`, 0) can be used to pad a String with zeros.
---

**Contents**

[TOC]

# Using String.format()

String.format() is a static method in the String class that can be used to pad a string with zeros.

Syntax: 

`String.format("%0[x]d", number);`

Where `x` is the total number of digits in the output string, and `number` is the number to be padded.

Example:

`String.format("%04d", 12);`

Output:

`0012`

# Using StringUtils.leftPad()

The StringUtils class in the Apache Commons Lang library provides a leftPad() method that can be used to pad a string with zeros.

Syntax: 

`StringUtils.leftPad(String str, int size, char padChar);`

Where `str` is the string to be padded, `size` is the total number of characters in the output string, and `padChar` is the character to use for padding.

Example:

`StringUtils.leftPad("12", 4, '0');`

Output:

`0012`
