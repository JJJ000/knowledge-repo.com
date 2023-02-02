---
title: What does a bare asterisk mean in function parameters?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-02 00:00:00
updated_at: 2023-02-02 00:00:00
tldr: A bare asterisk in function parameters in Python is used to indicate that a variable number of arguments can be passed to the function.
---

**Contents**

[TOC]

# Definition
A bare asterisk in function parameters in Python is a syntax used to pass an arbitrary number of arguments to a function. 

# Syntax
The syntax for a bare asterisk in function parameters is to place an asterisk (*) before the parameter name. 

# Example
For example, a function that takes an arbitrary number of arguments can be written as follows:

```
def example_func(*args): 
    for arg in args: 
        print(arg) 
```

# Usage
The asterisk is used to unpack the arguments. This means that all the arguments passed to the function are packed into a tuple. The asterisk unpacks the tuple so that the function can take in the arguments as separate values.
