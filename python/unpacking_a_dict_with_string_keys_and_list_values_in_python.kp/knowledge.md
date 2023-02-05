---
title: Iterating over a dictionary with a key of type string and a value of type list, there are too many elements to assign
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: Use a for loop to iterate over the dict, accessing each key and its corresponding list of values.
---

**Contents**

[TOC]

**Solution**

**Iterating over a Dictionary**

The most common way to iterate over a dictionary is to use a `for` loop. This loop will iterate over each key and value in the dictionary.

```
for key, value in my_dict.items():
    # Do something with key and value
```

**Avoiding 'Too Many Values to Unpack' Error**

When iterating over a dictionary, it is important to ensure that the number of variables in the loop matches the number of values being unpacked from the dictionary. If there are too many values being unpacked, the error `too many values to unpack` will be thrown.

To avoid this error, it is best to use the `dict.items()` method when iterating over a dictionary. This method will return a tuple of the key and value for each item in the dictionary. This ensures that the number of variables in the loop matches the number of values being unpacked.

```
for key, value in my_dict.items():
    # Do something with key and value
```

**Working with Lists as Values**

When iterating over a dictionary with a list as a value, it is important to note that the value will be returned as a list. To access the individual elements of the list, it is necessary to use a nested loop.

```
for key, value in my_dict.items():
    for element in value:
        # Do something with element
```
