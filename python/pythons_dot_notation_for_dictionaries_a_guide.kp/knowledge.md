---
title: What is the method for utilizing dot notation with dictionaries in python?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-16 00:00:00
updated_at: 2023-03-16 00:00:00
tldr: To access the value of a key in a dictionary using dot notation, use the name of the dictionary followed by a dot and then the key name with no quotes.
---

**Contents**

[TOC]

# Introduction

In Python, a dictionary is a collection of key-value pairs, where each key corresponds to a value. One way to access the values in a dictionary is using dot notation. This tutorial will explain dot notation and how to use it to access dictionary values in Python.

# Understanding Dot Notation

Dot notation is a way to access attributes or methods of an object. In Python, dictionaries can also be represented as objects. Each key in a dictionary can be considered as an attribute of that object. Using dot notation on a dictionary allows us to access the value of a key directly, by specifying the key as if it were an attribute of the dictionary.

# Example of Using Dot Notation

```python
# create a dictionary
person = {'name': 'John', 'age': 35, 'gender': 'male'}

# access values using dot notation
print(person.name)    # gives an error
print(person.age)     # prints 35
print(person.gender)  # prints 'male'
```

As we can see in the example above, we create a dictionary called `person` with three key-value pairs. To access the values of these keys, we use dot notation.

# Limitations of Dot Notation

One limitation of using dot notation for dictionaries is that it only works with keys that are valid Python identifiers. This means that keys that contain spaces or special characters cannot be accessed using dot notation.

Another limitation is that dot notation cannot be used to modify the values of a dictionary. Dot notation is read-only for dictionaries.

# Conclusion

In this tutorial, we have learned about dot notation and how to access values in a dictionary using dot notation. We have also discussed the limitations of using dot notation for dictionaries. Using dot notation can make our code more concise and easier to read when working with dictionaries.
