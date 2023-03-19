---
title: What is the correct way to check for the values none, true or false in Python variables?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-07 00:00:00
updated_at: 2023-03-07 00:00:00
tldr: To test if a variable is None, use `if variableName is None`, and to test if a boolean variable is True or False, use `if variableName`, and `if not variableName` respectively.
---

**Contents**

[TOC]

# Using if...elif statement

One way to test if a variable is None, True or False is by using an if...elif statement. This statement will check if the variable is None first, then if it is True and finally if it is False. Here's an example:

```python
my_variable = False

if my_variable is None:
    print("my_variable is None")
elif my_variable:
    print("my_variable is True")
else:
    print("my_variable is False")
```

This will output "my_variable is False", since the value of my_variable is False.

# Using the ternary operator

Another way to test if a variable is None, True or False is by using the ternary operator. This is a more concise way of writing an if...else statement. Here's an example:

```python
my_variable = None

result = "my_variable is None" if my_variable is None else "my_variable is True" if my_variable else "my_variable is False"

print(result)
```

This will output "my_variable is None", since the value of my_variable is None.

# Using the bool function

A third way to test if a variable is None, True or False is by using the bool function. This function will return True if the value of the variable is not None, False or an empty container. Here's an example:

```python
my_variable = True

if my_variable is None:
    print("my_variable is None")
elif bool(my_variable):
    print("my_variable is True")
else:
    print("my_variable is False")
```

This will output "my_variable is True", since the value of my_variable is True.

# Using the is operator

Finally, another way to test if a variable is None is by using the is operator. This operator checks if two variables refer to the same object in memory. Here's an example:

```python
my_variable = None

if my_variable is None:
    print("my_variable is None")
else:
    print("my_variable is not None")
```

This will output "my_variable is None", since the value of my_variable is None.
