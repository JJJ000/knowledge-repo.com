---
title: What is the way Python handles int and long?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-12 00:00:00
updated_at: 2023-03-12 00:00:00
tldr: In Python 3, int and long are unified into a single int type, which can handle arbitrarily large integers.
---

**Contents**

[TOC]

### Introduction
Python is a high-level programming language which is dynamically typed, interpreted and comes with dynamic semantics. Python supports two new built-in data types: int (for Integer) and long. There is no limit to the size of long integers.

### Integers in Python
Integers are the simplest and most commonly used numeric data type in Python. They are an immutable type which means that they cannot be modified once created. In Python, integers are objects and are stored in memory as an integer object. They behave in a similar way to mathematical integers and can be used for arithmetic operations such as addition, subtraction, multiplication and division.

Python automatically allocates and deallocates memory for integers. When an integer is created, Python allocates memory to store the value of the integer. When the integer is no longer needed, Python deallocates the memory that was allocated for the integer.

### Long Integers in Python
Python supports long integers, which are integers that have no upper or lower limit to their size. They can be as large as the available memory space allows. In Python 2, long integers were a separate type from integers, but in Python 3, they were merged into the integer type. In Python 3, all integers are automatically long integers.

When a long integer is created in Python, the memory required to store the integer is allocated dynamically. This means that the memory is allocated on demand as the integer grows in size. As long integers can grow to be extremely large, Python allocates and deallocates memory for long integers in a different way to integers. When a long integer grows in size, Python automatically allocates additional memory to store the new bits. When a long integer is no longer needed, Python deallocates the memory that was allocated for the integer.

### Conclusion
In Python, integers and long integers are used to represent numerical data. Integers are used to represent simple numerical values, while long integers can be used to represent extremely large numerical values. Python manages the memory allocation and deallocation for both integer and long integer objects differently. Because Python is a dynamically typed language, the type of integer or long integer is determined at runtime.
