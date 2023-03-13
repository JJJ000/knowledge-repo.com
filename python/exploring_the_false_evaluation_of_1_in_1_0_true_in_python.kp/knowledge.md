---
title: How come the expression '(1 in [1,0] == true)' results in false?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-13 00:00:00
updated_at: 2023-03-13 00:00:00
tldr: Because the `in` operator tests for membership in a sequence and 1 is a member of the list [1, 0], so the expression evaluates to True, but it is then compared to the integer value True, which is not equal to 1, resulting in False.
---

**Contents**

[TOC]

Type Coercion in Python

In Python, values of one type can be converted, or coerced, to another type. Coercion can happen implicitly or explicitly. 

The in keyword in Python

The in keyword is used to check if a value is present in a sequence such as a list, tuple, or string. 

Python's comparison operators

Python has various comparison operators, including == (equal to), > (greater than), and < (less than), which return a Boolean value of True or False depending on whether the comparison is true or false.

Explaining the Issue: 

When using the in keyword, Python checks if the value on the left exists in the sequence on the right. In this case, 1 exists in the list [1,0], so the expression (1 in [1,0]) should evaluate to True. 

However, we are comparing the result of the evaluation of the in keyword with the boolean True instead of the int type variable with value 1. 

When checking for equality using the == operator, Python considers the types of the values being compared. In this case, the type of the left-hand side expression is bool, while the type of the right-hand side expression is int. 

Since bool and int are different types, Python cannot convert bool to int implicitly. 

Thus, (1 in [1,0] == True) is equivalent to (True == True) which is True, but (1 in [1,0]) == int(True), which is False. 

Solution: 

To avoid this, we should use either of the following expressions: 

1. (1 in [1,0]) is True 

2. 1 in [1,0] == bool(True) 

Both expressions will evaluate to True, regardless of the type of the value being compared.
