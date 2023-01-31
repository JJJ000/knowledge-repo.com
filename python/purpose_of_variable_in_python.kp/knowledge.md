---
title: What is the meaning of using an underscore "_" as a variable name in python?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-01-30 00:00:00
updated_at: 2023-01-30 00:00:00
tldr: The single underscore `\_` variable is used as a temporary throwaway variable to store the result of the last expression in an interpreter session.
---

**Contents**

[TOC]

# Usage
The single underscore "_" variable is used as a placeholder for a variable that is not going to be used in the program.

# Examples
For example, in a for loop, the variable "_" can be used to loop through a list of values without having to use a variable name.

```python
for _ in range(10):
    print("Hello World")
```

Another example is when a function returns more than one value, the single underscore "_" can be used to ignore the values that are not needed.

```python
def generate_values():
    return 1, 2, 3

_, value2, _ = generate_values()
print(value2)
```

# Conventions
Using the single underscore "_" variable is a common convention in Python to indicate that the variable is temporary and will not be used. It is also used in other programming languages, such as JavaScript.
