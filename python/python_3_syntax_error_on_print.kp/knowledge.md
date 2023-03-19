---
title: An error in syntax occurred when attempting to print using Python 3
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: In Python 3.x, print is a function and must be called with parentheses around the arguments.
---

**Contents**

[TOC]

Section 1: Introduction
When writing code in Python 3, it is important to be aware of syntax errors that may occur. Syntax errors often occur when there is an issue with the structure or formatting of the code. One common syntax error in Python 3 occurs with the "print" statement.

Section 2: Explanation of the Error
In Python 3, "print" is a function rather than a statement. This means that if the "print" statement is not written in the correct format, a syntax error will occur. For example, if parentheses are not used around the printed values, a syntax error will be thrown. Additionally, if the printed values are not separated by commas, this will also result in a syntax error.

Section 3: Examples of Syntax Errors in Print Statements
Here are some examples of syntax errors that can occur with "print" statements in Python 3:

Example 1:
print "Hello, World!"
Output: SyntaxError: Missing parentheses in call to 'print'. Did you mean print("Hello, World!")?

Example 2:
print("Hello, World!"
Output: SyntaxError: unexpected EOF while parsing

Example 3:
print("Hello" "World")
Output: HelloWorld

Section 4: Conclusion
Overall, it is important to double-check the syntax of "print" statements in Python 3 to avoid common syntax errors. Remember to use parentheses around the printed values and separate them with commas. By avoiding syntax errors, you can write cleaner, more effective code in Python 3.
