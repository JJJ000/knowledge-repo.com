---
title: Reword using enumerate() with Python dictionaries
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-16 00:00:00
updated_at: 2023-03-16 00:00:00
tldr: The enumerate() function can be used to iterate through the items of a dictionary, but it will only return the index of each item, not the key-value pair.
---

**Contents**

[TOC]

Section 1: Introduction
The `enumerate()` function in python is used to loop over an iterable object while keeping track of the index of the current item being processed. However, the `enumerate()` function can only be used with iterable objects such as lists, tuples, and strings.

Section 2: Using enumerate() with dictionaries
Since dictionaries are not iterable objects, the `enumerate()` function cannot be used directly with them. In order to use `enumerate()` with a dictionary, we need to convert the dictionary into an iterable object.

Section 3: Converting dictionaries into iterable objects
We can convert a dictionary into an iterable object using any of the following methods:

1. Using the `dict.items()` method - This method returns a list of key-value pairs in the dictionary, which can be looped over using `enumerate()`.

2. Using the `dict.keys()` method - This method returns a list of keys in the dictionary, which can be looped over using `enumerate()`. We can then access the corresponding values using the keys.

3. Using the `dict.values()` method - This method returns a list of values in the dictionary, which can be looped over using `enumerate()`. We can then access the corresponding keys using the indices.

Section 4: Examples using enumerate() with dictionaries
Example 1: Using dict.items()
```
my_dict = {'a': 1, 'b': 2, 'c': 3}

for index, item in enumerate(my_dict.items()):
    print(index, item)
```
Output:
```
0 ('a', 1)
1 ('b', 2)
2 ('c', 3)
```

Example 2: Using dict.keys()
```
my_dict = {'a': 1, 'b': 2, 'c': 3}

for index, key in enumerate(my_dict.keys()):
    print(index, key, my_dict[key])
```
Output:
```
0 a 1
1 b 2
2 c 3
```

Example 3: Using dict.values()
```
my_dict = {'a': 1, 'b': 2, 'c': 3}

for index, value in enumerate(my_dict.values()):
    print(index, list(my_dict.keys())[list(my_dict.values()).index(value)], value)
```
Output:
```
0 a 1
1 b 2
2 c 3
```
