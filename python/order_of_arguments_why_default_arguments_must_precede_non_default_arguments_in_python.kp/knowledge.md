---
title: What is the reason for default arguments always preceding non-default arguments?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Non-default arguments must be placed before default arguments as specifying a default argument before a non-default argument would cause a syntax error.
---

**Contents**

[TOC]

1. Default Arguments
In Python, default arguments are a way to provide optional values for function arguments. Default arguments are specified in the function definition using an equal sign after the argument name, followed by the default value. When the function is called, if the argument is not provided, the default value is used.

2. Non-default Arguments
Non-default arguments are a required argument passed to a function. They are called positional arguments because their position in the function call determines the parameter they are passed to.

3. The Order of Arguments Matters
Python is a positional language when it comes to function arguments. That is, the order of arguments matters. If you switch the order of arguments in a function call, Python will interpret the arguments as belonging to different parameters. 

4. Why Non-default Arguments Cannot Follow Default Arguments
In Python, when default arguments are followed by non-default arguments, it can create ambiguity. If you were to define a function with a default argument, followed by a non-default argument, and the function was called without passing in the default argument, it would be unclear which parameter the non-default argument belongs to. To avoid this ambiguity, Python does not allow non-default arguments to follow default arguments.
