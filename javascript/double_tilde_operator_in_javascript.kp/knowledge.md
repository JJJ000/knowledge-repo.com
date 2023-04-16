---
title: What does the "double tilde" (~~) operator do in javascript?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: The double tilde (~~) operator is a bitwise operator in JavaScript that performs a type conversion and returns the integer part of a number.
---

**Contents**

[TOC]

## Definition
The double tilde (~~) operator is a bitwise operator in JavaScript that performs a bitwise NOT operation on a given number. It can be used to convert a number to its integer representation.

## Syntax
The syntax for the double tilde operator is as follows:

~~number

Where number is the number to be converted to an integer.

## Examples
Here are some examples of the double tilde operator in action:

~~3.14 // returns 3
~~3.99 // returns 3
~~-3.14 // returns -3

## Use Cases
The double tilde operator can be used to convert any given number to its integer representation. It can also be used to quickly check if a number is an integer or not. For example:

if(~~number === number) {
    // number is an integer
} else {
    // number is not an integer
}
