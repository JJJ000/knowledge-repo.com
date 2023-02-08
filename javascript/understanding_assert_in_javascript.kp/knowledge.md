---
title: What does "assert" mean in javascript?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-08 00:00:00
updated_at: 2023-02-08 00:00:00
tldr: Assert in JavaScript is a method used to test if a given statement is true or false.
---

**Contents**

[TOC]

## Definition

Assert is a keyword in JavaScript that is used to test a condition and throw an error if the condition is not met. This keyword is commonly used in unit testing to ensure that the code is working as expected.

## Syntax

The syntax for using assert in JavaScript is as follows:

```
assert(condition, message);
```

Where `condition` is the condition to be tested and `message` is an optional error message to be thrown if the condition is not met.

## Examples

Here are some examples of using assert in JavaScript:

```
// test if a number is greater than 5
assert(num > 5, "Number must be greater than 5");

// test if a string is not empty
assert(str !== "", "String must not be empty");
```

## Use Cases

Assert is commonly used in unit testing to ensure that the code is working as expected. It can also be used to validate user input or to check the state of a variable before performing an operation.
