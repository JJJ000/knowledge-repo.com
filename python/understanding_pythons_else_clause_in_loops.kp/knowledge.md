---
title: What is the way to comprehend the purpose of the "else" statement present in Python loops?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-08 00:00:00
updated_at: 2023-03-08 00:00:00
tldr: The `else` clause of Python loops is executed after the loop has been completely iterated through, unless the loop is exited early by a `break` statement.
---

**Contents**

[TOC]

# Introduction

In programming, there are situations where you need to perform different actions based on different conditions. Python provides a conditional statement called `if-else` that enables you to execute different blocks of code based on the Boolean value of an expression. In this tutorial, we'll explore the `else` clause in Python loops. 

# Python Loops and the `else` Clause

Loops are used to repeat a code block multiple times until a certain condition is met. Python provides three types of loops, namely `for`, `while`, and `do-while`. Loops can have an optional `else` clause that gets executed when the loop completes its iteration successfully, without being interrupted by a `break` statement. 

Here is the general syntax for a loop with an `else` clause:

```
for item in iterable:
    # Loop body
else:
    # Code block to be executed after the loop completes its iteration
```

In the above example, the `else` clause is executed after the `for` loop has completed its iteration successfully. If the loop is interrupted by a `break` statement, the `else` clause won't be executed.

# Example

Let's look at an example of a loop with an `else` clause:

```
numbers = [1, 2, 3, 4, 5]
for num in numbers:
    if num == 6:
        print("Number found!")
        break
else:
    print("Number not found!")
```

In the above example, we're iterating over a list of numbers. We check if the current number is equal to 6, and if so, we print a message and break out of the loop. If we don't find the number 6 in the list, we print a message to indicate that the number was not found. 

# Conclusion

In conclusion, the `else` clause in Python loops provides a way to execute a code block after the loop has completed its iteration successfully. If the loop is interrupted by a `break` statement, the `else` clause won't be executed. You can use this feature to perform cleanup operations or to execute code that should only be run after the loop has completed.
