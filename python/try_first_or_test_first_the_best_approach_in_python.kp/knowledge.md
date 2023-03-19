---
title: Is it preferable to attempt something and handle the exception or verify its feasibility beforehand to dodge an exception?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-13 00:00:00
updated_at: 2023-03-13 00:00:00
tldr: It is generally better to test if it`s possible first to avoid an exception in Python, rather than catching the exception after trying something.
---

**Contents**

[TOC]

Introduction
Python provides two ways to handle errors or exceptions, which are `try-except` blocks and if statements. In this article, we will discuss which of the two methods is better for handling errors in Python – trying something and catching the exception or testing if it’s possible first to avoid an exception.

Using Try-Except Blocks
`Try-except` blocks are the standard way of handling errors in Python. It involves trying or executing a block of code that may raise an exception, and catching any exception that was raised during execution. The advantage of using `try-except` blocks is that it allows you to handle errors gracefully, i.e., you can perform some cleanup or logging operations before the program exits due to an error.

Using If Statements
Another alternative to handling errors in Python is by using if statements. If statements involve testing if an operation is going to result in an exception, and if it does, you can opt to handle it or prompt the user about it. The key advantage of using if statements is that it allows you to handle errors earlier during code execution, i.e., before any significant resources are committed.

Comparing the Two Methods
When it comes to deciding which of the two methods is better for handling errors in Python, it depends on the use case. If you have a block of code that is going to perform some critical operation that may fail, then it’s wise to use `try-except` blocks. This is because you might need to perform some cleanup or logging operation before the program exits due to an error.

On the other hand, if you’re testing a user input or a function argument, you may want to use an if statement to handle any exception. When testing user inputs or function arguments, it’s always better to validate them upfront and reject invalid inputs at the front rather than trying and catching exceptions later.

Conclusion
In conclusion, both `try-except` blocks and if statements are valuable tools for handling errors in Python. It depends on the use case on which one is more effective. If you’re dealing with critical operations that may fail, it’s often best to use `try-except` blocks. However, if you’re testing user inputs, it’s always better to validate upfront using if statements before any significant resources are committed.
