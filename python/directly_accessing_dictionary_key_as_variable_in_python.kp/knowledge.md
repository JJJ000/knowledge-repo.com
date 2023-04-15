---
title: Is there a way to directly retrieve the dictionary key as a variable in Python without having to search for it through its value?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-16 00:00:00
updated_at: 2023-04-16 00:00:00
tldr: You can use the `keys()` method to obtain a list of keys and then access them by index or iteration.
---

**Contents**

[TOC]

Section 1: Introduction
There are various ways in Python to get the dictionary key as a variable. We can retrieve the dictionary key as a variable either by iterating over the dictionary keys, or we can make use of the inbuilt dictionary method keys() to get all the keys and store them in a variable. In this article, we shall discuss these two methods in detail.

Section 2: Retrieving dictionary key as a variable by iterating over the dictionary keys
To retrieve the dictionary key as a variable, we can make use of the for loop to iterate over the dictionary keys. We can store the variable as we iterate over the keys, and use it later in the code.

```
# Define the dictionary
dictionary = {'a': 1, 'b': 2, 'c': 3}

# Iterate over the dictionary
for key in dictionary.keys():
    stored_key = key
    # Further code goes here
```

In this code, we iterate over the dictionary keys using the for loop and store the key in the variable named stored_key. We can use this variable later in the code.

Section 3: Retrieving dictionary key as a variable using the keys() method
In Python, we can use the keys() method of the dictionary to get all the keys and store it in a variable. The keys() method returns an iterable view of the dictionary's keys. We can then use this variable to access dictionary keys anywhere in the code.

```
# Define the dictionary
dictionary = {'a': 1, 'b': 2, 'c': 3}

# Get all the keys using the keys() method
keys = dictionary.keys()

# Use the keys variable anywhere to access dictionary keys
print(keys)    # output {'a', 'b', 'c'}
```

In this code, we use the keys() method to get all the dictionary keys and store them in the variable named keys. We can then use this keys variable to access any dictionary key anywhere in our code.

Section 4: Conclusion
In this article, we discussed the two methods to get the dictionary key as a variable in Python. We can either use the for loop to iterate over the dictionary keys and store it in a variable or make use of the keys() method of the dictionary to get all the keys and store them in a variable. By following the above methods, we can easily retrieve the dictionary key as a variable in Python.
