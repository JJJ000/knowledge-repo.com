---
title: What is the procedure for obtaining a single character from the user?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: Use the built-in function input() to read a single character from the user in Python.
---

**Contents**

[TOC]

# 1. Using getpass.getpass()
The getpass.getpass() method allows the user to enter a single character from the keyboard in a secure manner. It reads the character as a string and masks the input from the user.

# 2. Using msvcrt Module
The msvcrt module can be used to read a single character from the user. It reads the character as it is typed and does not mask the input from the user.

# 3. Using the Input() Function
The input() function can also be used to read a single character from the user. It reads the character as a string and does not mask the input from the user.

# 4. Using the sys.stdin.read(1) Method
The sys.stdin.read(1) method can be used to read a single character from the user. It reads the character as a string and does not mask the input from the user.
