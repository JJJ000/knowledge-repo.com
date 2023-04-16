---
title: How can I generate a random boolean in python?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: random.choice([True, False])
---

**Contents**

[TOC]

#Generating a Random Boolean

##Using the Random Module
Python's `random` module provides a function `random.choice()` which can be used to generate a random boolean. This function takes a single argument which is a sequence (list, tuple, etc.) of boolean values from which to choose.

##Example
```python
import random

random_boolean = random.choice([True, False])
```

##Output
The output of the above code could be either `True` or `False` depending on the random selection.

##Conclusion
By using the `random.choice()` function, it is possible to generate a random boolean in Python.
