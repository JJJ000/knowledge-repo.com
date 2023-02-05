---
title: Retrieving the name of a variable as a string
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: Use the built-in function `eval()` to get the value of a variable whose name is passed as a string.
---

**Contents**

[TOC]

#Section 1: Using locals()
The locals() method can be used to get the names of all local variables in the current scope as a dictionary. To get the name of a variable as a string, the key of the dictionary can be used.

#Section 2: Example
```
def example_function():
    x = 10
    print(locals()['x'])

example_function()

# Output: 10
```

#Section 3: Using dir()
The dir() method can be used to get a list of the names of all variables in the current scope. To get the name of a variable as a string, the item in the list can be used.

#Section 4: Example
```
def example_function():
    x = 10
    print(dir()[1])

example_function()

# Output: x
```
