---
title: What is the reason that pylint deems the use of len(sequence) in condition values as inappropriate?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: Using len(SEQUENCE) in condition values is considered inefficient as it computes the length of the sequence on each iteration.
---

**Contents**

[TOC]

Introduction:
Pylint is a widely used tool for analyzing and checking code quality in Python. It is capable of detecting certain programming errors, such as syntax errors, semantic errors, and even stylistic errors. One of the common issues identified by Pylint is the use of len(SEQUENCE) in condition values. Let us delve deeper into the reasons behind it.

Section 1: Evaluating the length of a sequence 
The len() function is used to evaluate the length of a sequence in Python. Typically, this function is used to determine the number of items in a list, tuple, or string. For instance, if we have a list 'a', and we want to determine its length, we can use the len() function as len(a). 

Section 2: Use of len(SEQUENCE) in condition values 
One common programming practice is to use the len() function in condition values as a way of evaluating whether a sequence is empty or not. For example, consider the following code:

a = [1, 2, 3]
if len(a) == 0:
    print("a is empty")
else:
    print("a is not empty")

In the above code, we are checking whether the list 'a' is empty or not by evaluating its length. If it is equal to zero, we assume that the list is empty; otherwise, we assume that it is not empty. 

Section 3: The issue with using len(SEQUENCE) in condition values 
The use of len(SEQUENCE) in condition values is considered incorrect by Pylint for a few reasons. Firstly, it is a redundant operation. Evaluating the length of a sequence is an unnecessary step since it is possible to check if a sequence is empty by directly checking if it contains any elements. For example, we can simply use the following code to check if list 'a' is empty:

a = [1, 2, 3]
if not a:
    print("a is empty")
else:
    print("a is not empty")

Here, we are checking whether the list 'a' is empty by checking if it contains any elements. If not, it can be assumed that the list is empty. 

Section 4: Best practice
In conclusion, using len(SEQUENCE) in condition values is not considered best practice in Python. It is preferable to directly check if a sequence is empty or not using language features such as if not SEQUENCE. This not only simplifies the code but also makes it more efficient. 

As an AI language model, I need clarification to understand the reasoning process for the above answer.
