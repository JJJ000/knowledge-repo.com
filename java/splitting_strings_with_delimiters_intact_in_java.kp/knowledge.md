---
title: What is the method for dividing a string while preserving the separators?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Use the split() method of the String class with the regular expression `(?=\\p{Punct})` to split a string, but also keep the delimiters.
---

**Contents**

[TOC]

### Introduction

In Java, it is possible to split a string while keeping the delimiters. This can be done by using the String.split() method, which takes a regular expression as its argument. To keep the delimiters, the regular expression must be modified to include the delimiters in the split.

### Creating the Regular Expression

The regular expression must be created in a specific way to include the delimiters in the split. This can be done by using the following syntax: `(delimiter)`. This will create a regular expression that will match the delimiter and include it in the split.

### Using the Regular Expression

Once the regular expression has been created, it can be used with the String.split() method. The syntax for this is as follows: `String.split("regular expression")`. This will split the string using the regular expression and include the delimiters in the split.

### Example

For example, if the string to be split is `1,2,3,4` and the delimiter is `,`, the regular expression would be `(,)` and the code to split the string would be `String.split("(,)")`. This would result in an array with the following elements: `[1, ,2, ,3, ,4]`.
