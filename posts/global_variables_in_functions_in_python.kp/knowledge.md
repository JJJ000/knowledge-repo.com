---
title: Incorporating global variables into a function
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-18 00:00:00
updated_at: 2023-04-18 00:00:00
tldr: Global variables can be accessed and modified within a function in Python by declaring them with the keyword "global".
---

**Contents**

[TOC]

### Creating the Variable

Global variables in Python can be created by declaring a variable outside of any function, usually on the first line of code.

```python
x = 5
```

### Accessing the Variable

To access a global variable within a function, the keyword `global` must be used.

```python
def my_function():
  global x
  x += 1
  print(x)
```

### Modifying the Variable

When a global variable is modified inside a function, the change is reflected outside the function.

```python
def my_function():
  global x
  x += 1
  print(x)

my_function()
# Output: 6
```

### Caveats

It is important to note that global variables should be used sparingly, as they can lead to unexpected behavior and make code difficult to debug.
