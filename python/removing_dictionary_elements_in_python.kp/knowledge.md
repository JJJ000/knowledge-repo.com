---
title: Remove an item from a dictionary
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: Use the del keyword to delete an element from a dictionary in Python.
---

**Contents**

[TOC]

# Section 1 - Accessing Dictionary

In Python, a dictionary is a collection of key-value pairs. To access an element from a dictionary, you must use its associated key. 

# Section 2 - Deleting an Element

To delete an element from a dictionary, you can use the `del` statement. The syntax for deleting an element from a dictionary is `del dictionary[key]`, where `dictionary` is the name of the dictionary and `key` is the key of the element you want to delete.

# Section 3 - Examples

Let's say we have a dictionary called `my_dict` that contains the following elements:

```
my_dict = {
    "name": "John",
    "age": 30,
    "city": "New York"
}
```

To delete the element with the key `"age"`, we would use the following code:

```
del my_dict["age"]
```

# Section 4 - Output

After running the code, the dictionary `my_dict` would contain the following elements:

```
my_dict = {
    "name": "John",
    "city": "New York"
}
```
