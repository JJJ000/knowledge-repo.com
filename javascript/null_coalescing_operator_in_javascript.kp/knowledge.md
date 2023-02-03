---
title: Does JavaScript have a 'null coalescing' operator?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-02 00:00:00
updated_at: 2023-02-02 00:00:00
tldr: No, there is no null coalescing operator in JavaScript.
---

**Contents**

[TOC]

## What is a Null Coalescing Operator?
A null coalescing operator is a type of operator that is used to select the first non-null and non-undefined value from a sequence of operands. It is a type of short-circuiting operator, which means that it will only evaluate the second operand if the first one is null or undefined.

## Does JavaScript Have a Null Coalescing Operator?
No, JavaScript does not have a null coalescing operator. 

## What are Some Alternatives?
One alternative to a null coalescing operator in JavaScript is the logical OR operator (||). This operator will return the first truthy value from a sequence of operands, or the last operand if all of the preceding operands are falsy. 

Another alternative is the ternary operator (?:). This operator will return the second operand if the first operand is true, or the third operand if the first operand is false. This operator can be used to provide a default value if the first operand is null or undefined.
