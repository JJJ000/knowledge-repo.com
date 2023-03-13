---
title: How to use shorthand for if-else statements in python?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-13 00:00:00
updated_at: 2023-03-13 00:00:00
tldr: Python has a short-hand syntax for if-else statements known as the ternary operator, which allows you to write an if-else statement on one line.
---

**Contents**

[TOC]

1) Ternary Operator
The ternary operator is a shorthand way of writing an if-else statement in Python. It takes the form of condition_if_true if condition else condition_if_false. 

Example:
num = 5
message = "Number is even" if num % 2 == 0 else "Number is odd"
print(message)

Output:
Number is odd

2) Short-circuit Evaluation
Python also allows for short-circuit evaluation to achieve a shorthand if-else statement. It works by using the and or or operator to check the condition and evaluate the outcome based on the truthiness of the conditional statement.

Example:
num = 4
message = num % 2 == 0 and "Number is even" or "Number is odd" 
print(message)

Output:
Number is even

3) Dictionary
In Python, it is possible to use a dictionary to replace a switch-case statement. The keys represent the possible conditions, and the values are the corresponding outcomes.

Example:
num = 5
message_dict = {0: "Number is even", 1: "Number is odd"}
message = message_dict[num % 2]
print(message)

Output:
Number is odd

4) Chained Comparison
Python allows for chained comparisons to replace extensive if-else statements. By stringing together conditions with logical operators like and and or, it is easy to evaluate multiple conditions in a single line.

Example:
num = 5
message = "Number is even" if num % 2 == 0 else "Number is odd" if num % 2 == 1 else "Number is zero"
print(message)

Output:
Number is odd
