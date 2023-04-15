---
title: What causes early returns to be slower than other options?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-17 00:00:00
updated_at: 2023-04-17 00:00:00
tldr: Early return is not necessarily slower than else in Python, as it depends on the context and specific implementation.
---

**Contents**

[TOC]

# Introduction

In Python, `return` statements can be used to break out of a function and return a value to the caller. While it is generally accepted that using an early `return` statement can make code more readable, some people raise concern that early `return` statements can slow down code execution. In this answer, we will explore why early returns can be slower than else blocks in Python.

# Explanation

## Early returns require additional branching

When an early `return` statement is used in a Python function, execution immediately leaves the function and jumps back to the calling code. This means that the code in the function after the `return` statement is not executed. When this happens, the Python interpreter must create a new execution context and push it onto the call stack. When the function is called again, the interpreter must pop the execution context off the stack and continue interpreting the function. This additional branching can add overhead to the function and slow it down.

## Else blocks can optimize performance

When an `else` block is used instead of an early `return` statement, the code in the function can sometimes be optimized for better performance. For example, consider the following code:

```
def check_number(num):
    if num % 2 == 0:
        return "even"
    else:
        return "odd"
```

This code could also be written as:

```
def check_number(num):
    if num % 2 == 0:
        return "even"
    return "odd"
```

While both versions of the code are functionally equivalent, the first version uses an `else` block to reduce the amount of code that needs to be executed. In this case, the Python interpreter can optimize the code by avoiding the additional branching of the second version.

## Early returns can improve readability

While early returns can sometimes add overhead to code execution, they can also improve code readability. In some cases, an early return can make code more concise and easier to understand. For example, consider the following code:

```
def is_valid_input(input):
    if input is None:
        return False
    if input == "":
        return False
    if not input.startswith("http"):
        return False
    return True
```

This function could be written without early `return` statements, but the resulting code would be longer and harder to read. In this case, the increased readability of the early returns may be worth the additional overhead.

# Conclusion

Early returns can add overhead to code execution in Python, but they can also improve code readability. When deciding whether to use early returns or `else` blocks, it is important to balance performance and readability considerations. If performance is a major concern, `else` blocks may be the better choice. If readability is a major concern, early returns may be the better choice.
