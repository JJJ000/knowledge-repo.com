---
title: Comparing strings in Python is versus the double equals operator (==)
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-01 00:00:00
updated_at: 2023-02-01 00:00:00
tldr: The operator `is` checks if two variables point to the same object, whereas the operator `==` checks if the values of the two variables are equal.
---

**Contents**

[TOC]

### Definition

**is**: is operator in Python is used to check if two variables point to the same object. 

**==**: == operator in Python is used to check if the values of two operands are equal.

### Comparison

- **is** operator compares the memory locations of two objects, while **==** operator compares the values of two objects.

- **is** operator returns True if two variables point to the same object, whereas **==** operator returns True if two variables are of the same value.

### Usage

- **is** operator is used to check if two variables point to the same object, while **==** operator is used to check if two variables have the same value.

- When comparing strings, **is** operator checks if both strings are the same object, while **==** operator checks if both strings have the same value.
