---
title: Translating a Python dictionary into keyword arguments?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Pass the Python dict as the **kwargs argument to the function.
---

**Contents**

[TOC]

### Using `**` Operator
The `**` operator can be used to convert a Python dict to kwargs. This operator is used to unpack a dictionary to pass keyword arguments to a function. 

Example:
```python
def print_values(**kwargs): 
    for key, value in kwargs.items(): 
        print(key, " ", value) 
  
# Driver code 
dict = {'name':'John', 'age':24} 
  
# Unpacking dictionary 
print_values(**dict) 
```
Output:
```
name   John
age   24
```

### Using `dict.items()`
The `dict.items()` method can also be used to convert a Python dict to kwargs. This method returns a view object that displays a list of a given dictionary's (key, value) tuple pair. 

Example:
```python
def print_values(**kwargs): 
    for key, value in kwargs.items(): 
        print(key, " ", value) 
  
# Driver code 
dict = {'name':'John', 'age':24} 
  
# Converting to kwargs 
kwargs = dict(dict.items()) 
  
# Unpacking dictionary 
print_values(**kwargs) 
```
Output:
```
name   John
age   24
```
