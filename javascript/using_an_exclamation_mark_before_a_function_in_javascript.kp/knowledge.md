---
title: What is the purpose of the exclamation mark before the function?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-03 00:00:00
updated_at: 2023-02-03 00:00:00
tldr: The exclamation mark before a function in Javascript is used to denote a logical NOT operator.
---

**Contents**

[TOC]

# Definition
The exclamation mark (!) before a function in Javascript is known as a logical NOT operator. It is used to reverse the logical state of its operand.

# Usage
The logical NOT operator is typically used to check if a variable has a falsy value such as null, 0, undefined, empty string, or NaN. For example, if a variable is set to null, the logical NOT operator will return true.

# Syntax
The syntax for the logical NOT operator is as follows:
`!(expression)`

# Example
The following example shows how the logical NOT operator can be used to check if a variable is null:
`if (!myVariable) {
  //do something
}`
