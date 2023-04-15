---
title: What is the meaning of the '|=' operator?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: The pipe equal operator in Java is a compound assignment operator that assigns the result of a bitwise OR operation to a variable.
---

**Contents**

[TOC]

### Definition

The `|=` operator (also known as the pipe equal operator) is a compound assignment operator in Java which performs a bitwise OR operation and assigns the result to the left operand.

### Syntax

The syntax of the `|=` operator is as follows:

```java
variable |= expression;
```

Where `variable` is the left operand and `expression` is the right operand.

### Example

For example, consider the following code snippet:

```java
int x = 10;
x |= 5;
```

In this case, the expression `x |= 5` is equivalent to `x = x | 5`, which performs a bitwise OR operation on `x` and `5` and assigns the result back to `x`.

### Result

After executing this code, the value of `x` would be `15`, since the bitwise OR of `10` and `5` is `15`.
