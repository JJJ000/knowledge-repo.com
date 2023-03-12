---
title: How to iterate over all values in nested dictionaries?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-12 00:00:00
updated_at: 2023-03-12 00:00:00
tldr: You can loop through all nested dictionary values in Python by using nested loops and recursion.
---

**Contents**

[TOC]

### Introduction
In Python, nested dictionaries are dictionaries within a dictionary. They are also known as nested or multidimensional dictionaries. A nested dictionary is a dictionary inside a dictionary such that each key can have its key-value pairs. 

A nested dictionary can be useful in many cases where you might want to create a hierarchical structure, keep track of the data, data serialization, or data analysis. In this article, we will discuss how to loop through all nested dictionary values in Python.

### Loop through all nested dictionary values
To loop through all nested dictionary values, we can use a recursive function. The recursive function will iterate over each key-value pair of the dictionary and check if the value is a dictionary. If the value is a dictionary, we will call the same function again, passing the value as the argument.

```python
def print_values(dictionary):
    for value in dictionary.values():
        if isinstance(value, dict):
            print_values(value)
        else:
            print(value)
```

### Example
Let’s see an example of the above function in action:

```python
my_dict = {'a': {'b': {'c': 'd'}}}

print_values(my_dict)
```

Output:
```
d
```

### Conclusion
In this article, we have discussed how to loop through all nested dictionary values in Python using a recursive function. A recursive function is a function that calls itself until a base condition is met. We have also seen an example of how to use the function to iterate through all nested dictionary values.
