---
title: What is the syntax for an inline if statement in javascript?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: An inline IF statement in JavaScript is written using the ternary operator (condition ? expression1  expression2).
---

**Contents**

[TOC]

## Syntax

The syntax for an inline if statement in JavaScript is as follows:

`(condition) ? trueResult : falseResult;`

## Example

Here is an example of an inline if statement in JavaScript:

`var result = (age > 18) ? 'adult' : 'minor';`

In this example, the variable `result` will be assigned the value `adult` if the value of `age` is greater than 18, and `minor` if the value of `age` is less than or equal to 18.

## Explanation

The inline if statement is a shorthand way of writing an if-else statement in JavaScript. It consists of a condition, followed by a question mark (`?`), followed by the expression to execute if the condition is true, followed by a colon (`:`), followed by the expression to execute if the condition is false.

## Advantages

Using an inline if statement can help to make code more concise and easier to read, as it eliminates the need for an extra block of code (the else statement). It also allows for more complex conditions to be written in a single line, which can help to reduce the amount of code that needs to be written.
