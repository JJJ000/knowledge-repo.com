---
title: Increasing an integer value in Python by one using the increment operator (++)
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-01-30 00:00:00
updated_at: 2023-01-30 00:00:00
tldr: In Python, the increment operator (++) does not exist; instead, use the augmented assignment operator (+=) to increment a variable.
---

**Contents**

[TOC]

# Incrementing with ++

## What is ++

The ++ operator is a unary operator that adds 1 to an integer variable. It is an increment operator.

## How to Use ++

The ++ operator can be used in two ways, either as a prefix or as a postfix. 

### Prefix

When used as a prefix, ++ adds 1 to the value of the variable before the expression is evaluated.

```
int x = 5;
int y = ++x;

// x is 6, y is 6
```

### Postfix

When used as a postfix, ++ adds 1 to the value of the variable after the expression is evaluated.

```
int x = 5;
int y = x++;

// x is 6, y is 5
```
