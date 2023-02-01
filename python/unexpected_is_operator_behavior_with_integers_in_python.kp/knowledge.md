---
title: The "is" operator displays an unexpected result when used with integers
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-01 00:00:00
updated_at: 2023-02-01 00:00:00
tldr: The `is` operator in Python compares object identity rather than value, so two integers with the same value may not be considered equal.
---

**Contents**

[TOC]

#### Integer Caching 
In Python, integers between -5 and 256 are cached and stored in memory, so that when they are used again, they don't have to be created again. This means that when using the is operator on integers in this range, it will return True even if two variables point to the same object in memory.

#### Integer Comparison 
The is operator compares the identity of two objects, which is different from the == operator, which compares the values. Since integers in the range of -5 to 256 are cached, the is operator will return True even if the values of the two objects are different. 

#### Integer Mutability 
Unlike strings and tuples, integers are immutable, meaning that their value cannot be changed. This means that the is operator will always return True when comparing two integers, even if the values are different. 

#### Integer Memory Allocation 
When two integers are created, they are stored in different memory locations. However, when integers in the range of -5 to 256 are created, they are stored in the same memory location. This means that when the is operator is used on integers in this range, it will return True even if the values are different.
