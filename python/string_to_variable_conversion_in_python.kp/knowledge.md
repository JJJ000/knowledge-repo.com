---
title: Reword "transform a string into a variable identifier in python."
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-13 00:00:00
updated_at: 2023-03-13 00:00:00
tldr: It is not possible to convert a string to a variable name in Python, but you can use a dictionary to achieve similar functionality.
---

**Contents**

[TOC]

## Using `eval()`

One way to convert a string to a variable name in Python is by using the `eval()` function. This function takes a string as an argument and evaluates it as a Python expression, which means it can be used to access variables given their names as strings. Here is an example:

```python
# Define a variable
foo = 42

# Convert a string to a variable name
var_name = "foo"
var_value = eval(var_name)

# Print the result
print(var_value)  # Output: 42
```

However, it is important to note that using `eval()` can be dangerous and should be avoided in situations where the input string may come from an untrusted source, as it can execute arbitrary code.

## Using the `globals()` and `locals()` functions

Another way to convert a string to a variable name in Python is by using the `globals()` and `locals()` functions. These functions return a dictionary of all the global and local variables in the current scope, respectively, and can be used to access variables given their names as strings. Here is an example:

```python
# Define a variable
foo = 42

# Convert a string to a variable name using the `locals()` function
var_name = "foo"
var_value = locals()[var_name]

# Print the result
print(var_value)  # Output: 42

# Convert a string to a variable name using the `globals()` function
var_name = "foo"
var_value = globals()[var_name]

# Print the result
print(var_value)  # Output: 42
```

However, like with `eval()`, it is important to use caution when using `globals()` and `locals()` in situations where the input string may not be trusted.

## Using a dictionary

A safer way to convert a string to a variable name in Python is by using a dictionary. This involves creating a dictionary with the variable names as keys and the variable values as values, and then accessing the values using the keys. Here is an example:

```python
# Define a variable
foo = 42

# Create a dictionary of variable names and values
vars_dict = {"foo": foo}

# Convert a string to a variable name using the dictionary
var_name = "foo"
var_value = vars_dict[var_name]

# Print the result
print(var_value)  # Output: 42
```

This approach is safer than using `eval()` or `globals()` and `locals()`, as it does not execute arbitrary code or rely on variables in the current scope, and is therefore suitable for use with untrusted input. However, it requires more work to set up the dictionary and keep it up to date with the current variables in the program.

## Using the `getattr()` function

Finally, the `getattr()` function can be used to access attributes of objects given their names as strings. This can be useful when working with objects that have many attributes, like modules or classes. Here is an example:

```python
import math

# Access an attribute of the `math` module using `getattr()`
attr_name = "pi"
attr_value = getattr(math, attr_name)

# Print the result
print(attr_value)  # Output: 3.141592653589793
```

Similarly, we can use `getattr()` to access attributes of objects that we have defined ourselves, such as class instances. This approach is safe and efficient, as it avoids executing arbitrary code and is well-suited to working with complex objects.
