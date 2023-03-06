---
title: A secure way of retrieving the value of a deeply nested dictionary
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: Using the get() method with the key name and providing a default value in case the key is not present.
---

**Contents**

[TOC]

Section 1: Introduction

Python dictionaries are used to store key-value pairs. The keys in a dictionary are unique and immutable while values can be of any data type like numbers, strings, lists, or even other dictionaries. Sometimes, we need to get the value of a key that is nested inside another dictionary. In this article, we will discuss safe methods to get values of nested dictionaries in Python.

Section 2: Accessing Nested Dictionary Keys

To get the value of a key nested inside a nested dictionary, we need to access the nested dictionary first.

``` python
my_dict = {
    'key1': {
        'nested_key1': 'nested_value1',
        'nested_key2': 'nested_value2'
    },
    'key2': 'value2',
    'key3': {
        'nested_key3': {
            'nested_nested_key1': 'nested_nested_value1'
        }
    }
}
```

In the above example, we have a nested dictionary with three levels of nesting. To access the value of the nested key 'nested_key2', we can use the following code:

``` python
value = my_dict['key1']['nested_key2']
print(value) # Output: nested_value2
```

If the nested key doesn't exist, we will get a KeyError. So, we need to check if the nested key exists before accessing its value.

Section 3: Safely Accessing Nested Dictionary Keys

To safely access values of nested dictionary keys, we can use the `get()` method of the dictionary object. The `get()` method returns the value of a key if it exists, otherwise, it returns None.

``` python
value = my_dict.get('key1', {}).get('nested_key2')
print(value) # Output: nested_value2
```

The first parameter of the `get()` method is the key to be accessed. The second parameter is the default value to be returned if the key doesn't exist. We have passed an empty dictionary as the default value, so `get()` will return an empty dictionary if 'key1' doesn't exist. Then, we have again called `get()` method on the returned dictionary with 'nested_key2' as the key.

If we want to return a custom default value, we can replace the empty dictionary with it.

``` python
value = my_dict.get('key1', {}).get('nested_key3', 'default_value')
print(value) # Output: default_value
```

In the above code, 'key1' and 'nested_key3' don't exist in the dictionary, so `get()` returns the default value 'default_value'.

Section 4: Conclusion

In Python, dictionaries are widely used to store key-value pairs. Sometimes, we need to access keys nested inside another dictionary. We can use the `get()` method of the dictionary object to safely access nested dictionary keys. The `get()` method returns the value of a key if it exists, otherwise, it returns None or a default value specified by us.
