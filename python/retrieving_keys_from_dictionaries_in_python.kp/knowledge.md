---
title: Find the key associated with a given value in the dictionary
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-01-30 00:00:00
updated_at: 2023-01-30 00:00:00
tldr: You can use the built-in `dict.get()` function to get the key by value in a dictionary in Python.
---

**Contents**

[TOC]

# Using a for loop

The simplest way to get a key by value in a dictionary is to use a for loop. 

```
for key, value in dictionary.items():
    if value == search_value:
        return key
```

This method will iterate over the dictionary, comparing each value with the search value. If a match is found, the associated key is returned.

# Using the get() Method

The get() method can also be used to get a key by value in a dictionary. This method takes two arguments: the key and a default value to return if the key is not found.

```
key = dictionary.get(search_value, None)
```

If the search value is found in the dictionary, the associated key is returned. If the search value is not found, the default value (None in this example) is returned.

# Using the in Operator

The in operator can also be used to get a key by value in a dictionary. This operator returns a Boolean value indicating whether the specified key is present in the dictionary.

```
if search_value in dictionary:
    key = dictionary[search_value]
```

If the search value is found in the dictionary, the associated key is returned. If the search value is not found, the in operator returns False.
