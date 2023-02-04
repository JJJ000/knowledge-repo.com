---
title: What is the syntax for using the (conditional) operator in javascript?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-04 00:00:00
updated_at: 2023-02-04 00:00:00
tldr: The conditional operator is used to evaluate an expression and return one of two values depending on the result of the evaluation.
---

**Contents**

[TOC]

### Syntax
The syntax for the conditional operator is as follows:

`condition ? expression1 : expression2`

### Explanation
The conditional operator is a ternary operator that evaluates a condition and returns a value based on the condition. If the condition is true, expression1 is returned; if the condition is false, expression2 is returned.

### Example
For example, the following statement:

`var x = (age > 18) ? "adult" : "minor";`

will evaluate the condition (age > 18) and assign the value of "adult" to the variable x if the condition is true, and "minor" if the condition is false.
