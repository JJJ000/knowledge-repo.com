---
title: What is the process of creating a nested dictionary in python?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-07 00:00:00
updated_at: 2023-03-07 00:00:00
tldr: You can create a nested dictionary in Python by defining a dictionary within another dictionary using curly braces and colons.
---

**Contents**

[TOC]

## 1. Creating an empty nested dict

The first step in creating a nested dict is to create an empty dictionary. This can be done using the `{}` syntax. 

``` python
nested_dict = {}
```

Now we have an empty dictionary, but we want to add more dictionaries inside this one.

## 2. Adding dictionaries to the nested dict

To add dictionaries to the nested dict, we can simply create a new dictionary and assign it as a value to a key inside the parent dict. Here's an example:

``` python
nested_dict = {
    'dict1': {},
    'dict2': {}
}
```

Now we have two dictionaries inside our `nested_dict`, with the keys `dict1` and `dict2`.

## 3. Populating the nested dict

Now that we have the basic structure of our nested dict, we can start populating it with actual values. To add a value to a nested dictionary, we need to first access that dictionary using its key, and then add the value to that dictionary using another key. Here's an example:

``` python
nested_dict = {
    'dict1': {
        'key1': 'value1',
        'key2': 'value2'
    },
    'dict2': {
        'key3': 'value3',
        'key4': 'value4'
    }
}
```

Now we have four key-value pairs inside our nested dict.

## 4. Accessing values inside the nested dict

To access a value inside the nested dict, we need to use multiple keys in succession. We start with the key for the outermost dictionary, and then keep accessing inner dictionaries until we reach the value we need. Here's an example:

``` python
print(nested_dict['dict1']['key1'])
# Output: 'value1'
```

This code accesses the `dict1` dictionary inside `nested_dict`, and then gets the value for the key `key1` inside that dictionary. 

And that's it! That's all you need to know to create, populate, and access values inside a nested dict.
