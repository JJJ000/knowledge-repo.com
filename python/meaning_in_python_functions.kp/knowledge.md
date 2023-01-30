---
title: What is the purpose of the arrow symbol (->) in Python function definitions?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-01-30 00:00:00
updated_at: 2023-01-30 00:00:00
tldr: In Python, the `->` symbol is used to indicate the return type of a function.
---

**Contents**

[TOC]

# Definition

The -> operator in Python function definitions is known as the arrow operator. It is used to indicate the return type of a function. It is placed between the parameters and the return type.

# Syntax

The syntax for the arrow operator is as follows:

def function_name(parameter_list) -> return_type:
    # function body

# Example

For example, the following function takes two parameters, x and y, and returns an integer:

def add(x, y) -> int:
    return x + y
