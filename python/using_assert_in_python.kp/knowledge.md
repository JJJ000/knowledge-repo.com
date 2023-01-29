---
title: What does 'assert' do in python?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: Assert is used to verify that a certain condition is met and to raise an error if it is not.
---

**Contents**

[TOC]

# Purpose 
The purpose of the `assert` keyword in Python is to enable developers to test their assumptions about their code. It is used to raise an exception if a condition is not met, allowing developers to detect and debug the issue before the program continues.

# Syntax
The syntax for using `assert` is as follows:
```
assert <condition>, <error message>
```

# Examples
For example, if a developer is writing a program that requires a number to be greater than 0, they could use `assert` to ensure that the number is greater than 0.

```
x = 5
assert x > 0, "x must be greater than 0"
```

# Benefits
The benefit of using `assert` is that it allows developers to quickly and easily detect and debug issues in their code. By testing assumptions, developers can be sure that their code is behaving as expected, and can quickly identify and fix any issues.
