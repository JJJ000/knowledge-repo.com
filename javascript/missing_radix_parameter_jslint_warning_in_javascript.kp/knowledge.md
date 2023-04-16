---
title: Jslint is indicating that a radix parameter is missing
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: JSLint is pointing out that a function call is missing a parameter that specifies the base of a number being parsed.
---

**Contents**

[TOC]

#What is a Radix Parameter?
A radix parameter is an optional parameter that specifies the base of the number being converted. It is used when converting a number from one base to another.

#Why is the Radix Parameter Important?
The radix parameter is important because it ensures that the number is converted correctly. Without it, the number may be converted incorrectly. For example, if you are converting a binary number (base 2) to a decimal number (base 10) and you do not specify the radix parameter, the conversion may not be correct.

#What Does JSLint Mean by "Missing Radix Parameter"?
JSLint is warning you that you are not specifying the radix parameter when converting a number from one base to another. Without the radix parameter, the conversion may be incorrect.

#How Do I Fix the Problem?
To fix the problem, you need to specify the radix parameter when converting a number from one base to another. For example, if you are converting a binary number (base 2) to a decimal number (base 10), you would use the following code: 

parseInt(binaryNumber, 2);
