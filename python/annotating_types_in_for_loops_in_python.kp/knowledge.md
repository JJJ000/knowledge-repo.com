---
title: What is the way to add type annotations in a for-loop?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: Use the colon and specify the type of the iterator variable after it, for example `for I int in range(10)` to annotate the type of the iterator variable in a for-loop in Python.
---

**Contents**

[TOC]

Section 1: Understanding the for-loop in Python
A for-loop in Python is a statement that provides a convenient way of running through items in a sequence or an iterable. It takes the form of a header line, followed by an indented block of code. The header line consists of the for keyword, followed by a variable name, the in keyword, and an iterable object.

Section 2: Annotating the types of variables in a for-loop
To annotate the type of a variable in a for-loop in Python, the syntax is similar to that used to annotate variables outside of a for-loop. We start by specifying the variable name, followed by a colon, and then the type of the variable. The type annotation is optional in Python but can add valuable documentation to your code.

Section 3: Example of annotating types in a for-loop
Consider the following example of a for-loop in Python that iterates over a list of integers and prints each item:

```python
numbers = [1, 2, 3, 4, 5]
for number in numbers:
    print(number)
```

To annotate the type of the variable number, we simply add a type annotation to the end of the variable name in the header line of the for-loop:

```python
numbers: List[int] = [1, 2, 3, 4, 5]
for number in numbers:
    print(number)
```

Now, the variable numbers is annotated as a List of integers, and Python's type checker will ensure that we only pass integers into the list.

Section 4: Conclusion
Annotating the types of variables in a for-loop in Python is an easy process that can provide valuable documentation to your code. By specifying the variable name, followed by a colon and then the type of the variable, we can ensure that we only use the variable in a way that is consistent with its intended purpose.
