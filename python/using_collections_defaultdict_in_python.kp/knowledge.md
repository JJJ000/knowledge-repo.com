---
title: What is the functionality of collections.defaultdict?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-01-30 00:00:00
updated_at: 2023-01-30 00:00:00
tldr: Collections.defaultdict is a dictionary-like container that returns a default value if a key is not found.
---

**Contents**

[TOC]

# Overview

Collections.defaultdict is a subclass of the built-in dict class. It is a container that provides fast key look-up with a default value when the key is not present. It is useful for creating dictionaries with default values, or for accessing elements of a dictionary with a default value if the key is not found.

# Usage

The defaultdict class is initialized with a default factory, which is used to create values for keys that are not already present in the dictionary. The default value is returned when the key is not found. The default factory can be any callable object, such as a function, a lambda expression, or a class.

# Example

For example, the following code creates a defaultdict with the default factory set to the int function, which returns the integer 0 when a key is not found:

```
from collections import defaultdict

my_dict = defaultdict(int)

# Accessing an element with a key that is not present
print(my_dict['key']) # prints 0
```

# Advantages

The main advantage of using defaultdict is that it is much faster than using the dict.get() method to access elements with a default value. It also allows for more concise code, as the default value does not need to be explicitly specified.
