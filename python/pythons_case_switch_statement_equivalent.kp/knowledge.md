---
title: What is the Python equivalent of a switch/case statement?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-01-30 00:00:00
updated_at: 2023-01-30 00:00:00
tldr: The Python equivalent for a case/switch statement is a series of if/elif/else statements.
---

**Contents**

[TOC]

**Option 1: Using If-Elif-Else**

The Python equivalent to a case/switch statement is an if-elif-else statement. This statement allows for multiple conditions to be checked and for different blocks of code to be executed depending on the result of the conditions.

For example, if we wanted to check a variable for three different values, we could do the following:

```
if x == 1:
    # do something
elif x == 2:
    # do something else
elif x == 3:
    # do something different
else:
    # do something else again
```

**Option 2: Using Dictionaries**

Another option for the Python equivalent of a case/switch statement is to use a dictionary. This option allows for a more concise syntax to be used, and it allows for the code to be more readable.

For example, if we wanted to check a variable for three different values, we could do the following:

```
switch = {
    1: do_something,
    2: do_something_else,
    3: do_something_different
}

switch.get(x, do_something_else_again)()
```

**Option 3: Using a Dictionary and a Function**

The final option for the Python equivalent of a case/switch statement is to use a dictionary and a function. This option allows for a more concise syntax to be used, and it allows for the code to be more readable.

For example, if we wanted to check a variable for three different values, we could do the following:

```
def switch(x):
    switcher = {
        1: do_something,
        2: do_something_else,
        3: do_something_different
    }
    return switcher.get(x, do_something_else_again)

switch(x)
```
