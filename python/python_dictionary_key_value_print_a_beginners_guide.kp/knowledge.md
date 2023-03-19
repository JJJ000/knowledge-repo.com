---
title: What is the method to output the key-value pairs of a dictionary in python?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: Use a for loop to iterate over the dictionary and print each key-value pair using the syntax keyvalue.
---

**Contents**

[TOC]

Section 1: Introduction
In Python, a dictionary is a collection of key-value pairs. It can be used to store and retrieve data in a more efficient way than using lists or other data structures. In this guide, we will discuss how to print the key-value pairs of a dictionary in Python.

Section 2: Using a for loop to print key-value pairs
One way to print the key-value pairs of a dictionary in Python is to use a for loop. We can iterate over the items of the dictionary and print the key and its corresponding value:

```
my_dict = {'key1': 'value1', 'key2': 'value2', 'key3': 'value3'}

for key, value in my_dict.items():
    print(key, value)
```

This will output:

```
key1 value1
key2 value2
key3 value3
```

Here, we are using the `items()` method of the dictionary to get a list of its items. The `items()` method returns a list of tuples, where each tuple contains a key-value pair of the dictionary. We are then unpacking each tuple into the `key` and `value` variables and printing them.

Section 3: Printing only keys or values of a dictionary
If we only want to print the keys or values of a dictionary, we can use the `keys()` or `values()` method of the dictionary, respectively. For example:

```
my_dict = {'key1': 'value1', 'key2': 'value2', 'key3': 'value3'}

# Print only keys
for key in my_dict.keys():
    print(key)

# Output: 
# key1
# key2
# key3

# Print only values
for value in my_dict.values():
    print(value)

# Output:
# value1
# value2
# value3
```

Here, we are using the `keys()` and `values()` methods of the dictionary to get a list of its keys and values, respectively. We are then iterating over each item of the list and printing it.

Section 4: Using pprint module to print a dictionary
If we have a nested dictionary or a dictionary with a large number of key-value pairs, it may be helpful to use the `pprint` module to pretty-print the dictionary. The `pprint` module provides a `pprint()` function that can be used to print a dictionary in a more readable format. For example:

```
import pprint

my_dict = {'key1': {'subkey1': 'value1', 'subkey2': 'value2'}, 
           'key2': {'subkey3': 'value3', 'subkey4': 'value4'}}

pprint.pprint(my_dict)
```

This will output:

```
{'key1': {'subkey1': 'value1', 'subkey2': 'value2'},
 'key2': {'subkey3': 'value3', 'subkey4': 'value4'}}
```

Here, we are using the `pprint()` function of the `pprint` module to pretty-print the dictionary. The output is indented and the nested dictionaries are shown in a more readable format.
