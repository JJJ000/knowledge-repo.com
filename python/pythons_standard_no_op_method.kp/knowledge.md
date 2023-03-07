---
title: Is there a conventional method for performing a no-op in python?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-07 00:00:00
updated_at: 2023-03-07 00:00:00
tldr: The standard way to do a no-op in Python is to use the `pass` statement.
---

**Contents**

[TOC]

Using pass statement

The pass statement is used in Python as a null operation when you need to perform no operation. Pass means, “do nothing.” The statement is useful in a situation where your program syntax requires an expression but you do not have anything to do or something to fill. It does not perform any action and returns none.

Example:

```
def my_function():
    pass

```
Using ellipsis

The ellipsis(...), also known as the “dot-dot-dot,” is a built-in Python object used as a placeholder. It is commonly used as a placeholder when the code is still being written, but should be added later. It is used for slicing, and in other cases when deriving a range of values.

Example:

```
my_list = [1, 2, 3, ...]
```

Using comments

Comments are a great way to explain what is going on in a program. They are used to mark certain parts of the code as essential or to add extra information to a section of code. In this case, comments can be used to create a no-op. Since comments are not executed, the code following the comment will be ignored.

Example:

```
def my_function():
    # This is a no-op
    print("This function does nothing")
```

Using True/False statements

Boolean statements in Python, such as True and False, can be used to perform no operations. Since they are not actually doing anything, they can be used to fill in a place where a statement is required.

Example:

```
if my_list:
    pass
```
Here, the if statement requires a statement to be executed if the condition is true. Since we don’t want to do anything, we use pass.
