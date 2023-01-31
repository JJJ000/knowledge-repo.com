---
title: What is the purpose of the "else" clause in the "try" statement in python?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-01-30 00:00:00
updated_at: 2023-01-30 00:00:00
tldr: The optional `else` clause of the `try` statement in Python is used to execute a block of code if no exceptions are raised in the `try` block.
---

**Contents**

[TOC]

1. Overview
------------------------
The optional "else" clause of the "try" statement in Python is used to define a block of code to be executed if no errors occur within the "try" block.

2. Syntax
------------------------
The syntax of the "try" statement with the "else" clause is as follows:

try:
    # code to be executed
except:
    # code to be executed if an error occurs
else:
    # code to be executed if no errors occur

3. Example
------------------------
For example, the following code will try to open a file, and if no errors occur, it will print out the contents of the file:

try:
    f = open("myfile.txt")
except:
    print("Error opening file")
else:
    print(f.read())

4. Benefits
------------------------
Using the "else" clause of the "try" statement allows for cleaner code that is easier to read and debug. It also allows for more efficient execution of code, as the code in the "else" clause will only be executed if no errors occur.
