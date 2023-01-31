---
title: What is the purpose of using 'else' after for and while loops in python?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-01-30 00:00:00
updated_at: 2023-01-30 00:00:00
tldr: Python uses `else` after for and while loops to execute a block of code when the loop condition is not met.
---

**Contents**

[TOC]

#Purpose
The purpose of the else statement is to provide an alternate set of instructions to be executed when the loop condition is not met.

#Syntax
The else statement is usually placed after a for or while loop. It is written in the following format:

for <item> in <sequence>:
    <statement(s)>
else:
    <statement(s)>

#Benefits
Using an else statement after a for or while loop allows for greater control over the flow of the program. It allows for the execution of code only when certain conditions are met. Additionally, it eliminates the need for additional conditional statements.

#Example
For example, consider the following code:

numbers = [1,2,3,4,5]

for num in numbers:
    if num % 2 == 0:
        print(num)
else:
    print("No even numbers found")

In this example, the else statement is used to print a message if no even numbers are found in the list. Without the else statement, the program would simply terminate without providing any feedback.
