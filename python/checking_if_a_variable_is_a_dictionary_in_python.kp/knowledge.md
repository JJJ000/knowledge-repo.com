---
title: What is the process for determining if a variable is a dictionary in python?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: You can check if a variable is a dictionary by using the type() function to check if the variable is of type dict.
---

**Contents**

[TOC]

# Using the type() Method

The type() method can be used to check if a variable is a dictionary, by passing the variable as an argument to the type() method. If the variable is a dictionary, the type() method will return a <class 'dict'> value.

```python
# Declaring a dictionary
dict_var = {
    "name": "John",
    "age": 24
}

# Checking if 'dict_var' is a dictionary
type_of_dict_var = type(dict_var)

# Print the type
print(type_of_dict_var)

# Output: <class 'dict'>
```

# Using the isinstance() Method

The isinstance() method can be used to check if a variable is a dictionary, by passing the variable and the dictionary type as arguments to the isinstance() method. This will return a boolean value (True or False) depending on whether the variable is a dictionary or not.

```python
# Declaring a dictionary
dict_var = {
    "name": "John",
    "age": 24
}

# Checking if 'dict_var' is a dictionary
is_dict_var = isinstance(dict_var, dict)

# Print the boolean value
print(is_dict_var)

# Output: True
```

# Using the dict() Constructor

The dict() constructor can be used to check if a variable is a dictionary, by passing the variable as an argument to the dict() constructor. If the variable is a dictionary, the dict() constructor will return a dictionary object.

```python
# Declaring a dictionary
dict_var = {
    "name": "John",
    "age": 24
}

# Checking if 'dict_var' is a dictionary
dict_obj = dict(dict_var)

# Print the dictionary object
print(dict_obj)

# Output: {'name': 'John', 'age': 24}
```
