---
title: What is the syntax for using the "pass" statement?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-02 00:00:00
updated_at: 2023-02-02 00:00:00
tldr: The `pass` statement in Python is used as a placeholder when no action is required, allowing the code to compile without any errors.
---

**Contents**

[TOC]

# Introduction

The “pass” statement is a special statement in Python that is used to indicate that nothing should be done. It is a null statement, and is used to prevent the interpreter from showing an error when a statement is syntactically correct but contains no operations.

# Syntax

The syntax for the pass statement is simply “pass”. It does not take any arguments or parameters.

# Usage

The pass statement is primarily used as a placeholder in compound statements such as if, while, and for statements. It can also be used in functions, classes, and modules. 

# Example

For example, the following code will print out the numbers from 1 to 10:

```
for i in range(1, 11):
    if i % 2 == 0:
        print(i)
    else:
        pass
```

The output of this code will be:

2
4
6
8
10
