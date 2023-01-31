---
title: What are the distinctions between the range and xrange functions in Python 2.x?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-01-30 00:00:00
updated_at: 2023-01-30 00:00:00
tldr: The range function returns a list, while the xrange function returns an iterator.
---

**Contents**

[TOC]

# Range Function
The range function returns a list of numbers that range from 0 up to a specified number. 

# Xrange Function
The xrange function returns an iterator that generates numbers on demand, rather than creating a list of all the numbers at once. 

# Key Differences
- The range function returns a list, while xrange returns an iterator. 
- The range function will create the entire list of numbers before returning them, while xrange only generates the numbers on demand. 
- The range function is slightly slower than xrange, since it has to create the entire list of numbers before returning them. 
- The xrange function is only available in Python 2.X, while the range function is available in both Python 2.X and Python 3.X.
