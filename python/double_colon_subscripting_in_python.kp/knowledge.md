---
title: What does the double colon () mean when used for subscripting sequences in python?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: In Python, double colons () when subscripting sequences indicate an inclusive range of elements from the beginning to the end of the sequence.
---

**Contents**

[TOC]

# Syntax
The double colon (::) is a slice operator in Python. It is used to slice sequences such as strings, lists, and tuples. It is used to select a range of items from a sequence. 

# Usage
The syntax for using the double colon is as follows: 

sequence[start:stop:step]

Where start is the starting index of the sequence, stop is the ending index of the sequence, and step is the amount by which the index should increment.

# Examples
For example, if we have the following list:

list = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]

We can use the double colon to select a range of items from the list. To select the first five items from the list, we can use the syntax:

list[0:5:1]

This will return the following:

[1, 2, 3, 4, 5]
