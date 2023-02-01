---
title: How do eval, exec, and compile differ from one another?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-01 00:00:00
updated_at: 2023-02-01 00:00:00
tldr: Eval evaluates a string containing a valid expression, Exec executes a string containing Python code, and Compile compiles a string containing Python code into a code object.
---

**Contents**

[TOC]

#### Eval
Eval is a built-in function in Python that takes a string and evaluates it as a Python expression. This means that it takes a string of Python code and runs it as if it were normal Python code. Eval is often used to quickly evaluate a single expression.

#### Exec
Exec is a built-in function in Python that takes a string and executes it as a Python statement. This means that it takes a string of Python code and runs it as if it were normal Python code. Exec is often used to execute multiple lines of code at once.

#### Compile
Compile is a built-in function in Python that takes a string and compiles it into a Python code object. This means that it takes a string of Python code and compiles it into a code object which can be executed later. Compile is often used to compile a string of Python code into a code object for later execution.
