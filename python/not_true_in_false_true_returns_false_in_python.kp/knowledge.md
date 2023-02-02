---
title: What is the result of evaluating "not(true) in [false, true]"?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-01 00:00:00
updated_at: 2023-02-01 00:00:00
tldr: Because `not(True)` evaluates to False, which is not in the list [False, True].
---

**Contents**

[TOC]

# Boolean Logic
Python uses boolean logic to evaluate expressions. The expression "not(True) in [False, True]" is evaluated as follows: 

1) not(True) evaluates to False
2) False is in [False, True]
3) Therefore, the expression evaluates to False

# List Syntax
Python uses brackets [] to denote lists. The expression "not(True) in [False, True]" is checking if the boolean value False is in the list [False, True].

# Membership Operator
Python uses the in operator to check if an element is present in a list. The expression "not(True) in [False, True]" is using the in operator to check if False is in the list [False, True].

# Return Value
Since False is in the list [False, True], the expression "not(True) in [False, True]" returns False.
