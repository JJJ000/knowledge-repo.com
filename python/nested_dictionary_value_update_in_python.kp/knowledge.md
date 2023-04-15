---
title: Modify the value of a nested dictionary that may have varying levels of depth
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-16 00:00:00
updated_at: 2023-04-16 00:00:00
tldr: To update the value of a nested dictionary of varying depth in Python, you can use a combination of key indexing and recursion.
---

**Contents**

[TOC]

Section 1: Introduction
--------------------------

In Python, dictionaries are commonly used to store and manage data. A nested dictionary is a dictionary that contains other dictionaries as its values.

If we have a nested dictionary, we may need to update the value of one of its keys. Updating the value of a nested dictionary can be a bit tricky because of the nested structure.

In this tutorial, we will discuss how to update the value of a nested dictionary of varying depth in Python.


Section 2: Accessing values in a nested dictionary
--------------------------------------------------------

Before we can update the value of a key in a nested dictionary, we need to know how to access the value that we want to update.

In Python, we can access the value of a key in a dictionary using the square bracket notation. If the dictionary is nested, we can chain square brackets to access the value.

For example, if we have this nested dictionary:

```
nested_dict = {
    'a': {
        'b': {
            'c': 1
        }
    }
}
```

We can access the value of the 'c' key using the following code:

```
nested_dict['a']['b']['c']
```

This code will return the value 1.



Section 3: Updating the value of a key in a nested dictionary
---------------------------------------------------------------

Once we have accessed the value that we want to update, we can simply assign a new value to it using the same square bracket notation.

For example, to update the value of the 'c' key in the nested_dict dictionary, we can use the following code:

```
nested_dict['a']['b']['c'] = 2
```

This code will update the value of the 'c' key to 2.



Section 4: Handling missing keys in a nested dictionary
-----------------------------------------------------------

If the key that we want to update does not exist in the nested dictionary, we will get a KeyError.

To handle this error, we can use the setdefault() method of dictionaries. The setdefault() method returns the value of the specified key if it exists in the dictionary. If the key does not exist, setdefault() adds the key with the specified value to the dictionary.

For example, if we want to update the value of the 'd' key in the nested_dict dictionary, which does not exist, we can use the following code:

```
nested_dict.setdefault('a', {}).setdefault('b', {})['d'] = 3
```

This code will add the 'd' key with the value 3 to the nested dictionary. The setdefault() method is used to create the missing nested dictionaries. The {} argument specifies an empty dictionary that is used as the default value for the setdefault() method.
