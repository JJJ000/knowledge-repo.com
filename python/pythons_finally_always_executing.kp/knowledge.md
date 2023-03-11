---
title: Is it guaranteed that 'finally' will execute in python?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-11 00:00:00
updated_at: 2023-03-11 00:00:00
tldr: No, `finally` block only executes when the try block is executed and exception is raised or not.
---

**Contents**

[TOC]

Yes, `finally` always executes in Python, except in certain rare cases. This behavior is guaranteed by the language specification itself. Below are some reasons why `finally` might not execute, and how they can be addressed.

## Exceptions in `finally` clause

If an exception occurs in the `finally` block, it will override any previous exceptions raised by the `try` or `except` blocks. This means that the original exception may be lost, and the program may terminate without executing any further code.

To avoid this, it is recommended to avoid raising exceptions in `finally` blocks. Instead, use `try/except` blocks inside the `finally` block to handle any potential errors.

## Terminating the program

In some rare cases, the program may terminate before the `finally` block is executed. This can happen if the interpreter is terminated unexpectedly, such as in the case of a power outage or a system crash.

In these situations, `finally` may not execute because the interpreter has already been terminated. There is not much that can be done to prevent this, other than ensuring that the program is well-designed and properly tested.

## Using exit() or os._exit()

If the exit() or os._exit() function is used in the `try` or `except` blocks, the `finally` block will not be executed. These functions are specifically designed to immediately terminate the program, without executing any further code.

To ensure that the `finally` block is executed in these cases, it is recommended to use `sys.exit()` instead. This function allows the current script to exit with a status code, but also ensures that the `finally` block is executed before exiting. 

## Conclusion

In summary, `finally` blocks are guaranteed to execute in Python unless the interpreter is terminated unexpectedly, an exit function is used, or an error is raised within the `finally` block itself. With proper error handling and testing, it is possible to avoid these situations and ensure that `finally` always executes as expected.
