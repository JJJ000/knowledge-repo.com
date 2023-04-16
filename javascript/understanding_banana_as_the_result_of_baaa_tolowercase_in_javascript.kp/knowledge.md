---
title: What is the output of applying the .tolowercase() method to the string 'b'+'a'+ + 'a' + 'a'?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: The plus symbols are being used to concatenate the strings, which results in `baa` being combined with `aa` to form `banana`.
---

**Contents**

[TOC]

# Explanation
The result of ('b'+'a'+ + 'a' + 'a').toLowerCase() is 'banana' because of the following:

## String Concatenation
In Javascript, the '+' operator is used for string concatenation. This means that when two strings are added together with the '+' operator, the strings are combined into a single string. In this case, the strings 'b', 'a', and 'a' are added together to form the string 'baaa'.

## toLowerCase() Method
The toLowerCase() method is a built-in Javascript function that converts all the characters in a string to lowercase. In this case, the string 'baaa' is converted to 'banana'.
