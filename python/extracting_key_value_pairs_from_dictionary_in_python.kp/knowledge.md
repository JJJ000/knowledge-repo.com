---
title: Retrieve a selection of key-value pairs from the dictionary?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-02 00:00:00
updated_at: 2023-02-02 00:00:00
tldr: You can extract a subset of key-value pairs from a dictionary in Python by using the dict.items() method.
---

**Contents**

[TOC]

**Section 1: Create a Dictionary**

Consider the following dictionary:

my_dict = {
    'name': 'John',
    'age': 25,
    'city': 'New York',
    'country': 'USA'
}

**Section 2: Extract a Subset of Key-Value Pairs**

To extract a subset of key-value pairs from the dictionary, we can use the `dict.items()` method. This method returns a list of tuples, where each tuple consists of a key-value pair.

For example, to extract the key-value pairs for name and age, we can do the following:

subset_dict = dict(my_dict.items()[:2])

This will return a dictionary with the following key-value pairs:

subset_dict = {
    'name': 'John',
    'age': 25
}

**Section 3: Using List Comprehension**

We can also use list comprehension to extract a subset of key-value pairs from the dictionary. For example, to extract the key-value pairs for city and country, we can do the following:

subset_dict = {key:value for key, value in my_dict.items() if key in ['city', 'country']}

This will return a dictionary with the following key-value pairs:

subset_dict = {
    'city': 'New York',
    'country': 'USA'
}

**Section 4: Using Dictionary Comprehension**

We can also use dictionary comprehension to extract a subset of key-value pairs from the dictionary. For example, to extract the key-value pairs for name and age, we can do the following:

subset_dict = {key:my_dict[key] for key in ['name', 'age']}

This will return a dictionary with the following key-value pairs:

subset_dict = {
    'name': 'John',
    'age': 25
}
