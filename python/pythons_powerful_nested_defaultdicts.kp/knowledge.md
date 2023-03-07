---
title: Defaultdict of defaultdict within another defaultdict
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-07 00:00:00
updated_at: 2023-03-07 00:00:00
tldr: Nested defaultdict of defaultdict in Python is a defaultdict that enables the creation of multi-level dictionaries with default values.
---

**Contents**

[TOC]

Introduction

A defaultdict is a subclass of Python's built-in dictionary class. It overrides one method, __missing__(), to provide a default value for a nonexistent key. When using a defaultdict, if you try to access a nonexistent key, the dict will not raise a KeyError but instead return the default value specified when creating the default dict. Nested defaultdict is a very useful data structure in Python. It provides a fast and convenient way of storing and accessing complex data.

Creating a nested defaultdict

We can create a nested defaultdict of defaultdict in Python by first creating a defaultdict and specifying defaultdict as the default factory. We can then create new nested defaultdict objects as dictionary values for each key in the outer defaultdict. The following code snippet shows how to create and use a nested defaultdict in Python:

```
from collections import defaultdict

d = defaultdict(lambda: defaultdict(int))

d['a']['b'] = 1
d['a']['c'] = 2
d['d']['e'] = 3

print(d['a']['b'])  # Output: 1
print(d['a']['c'])  # Output: 2
print(d['d']['e'])  # Output: 3
```

In this example, we've created a nested defaultdict with default factory int. The inner defaultdict objects will be automatically created when we first try to access them. If we try to access a nonexistent inner key, the default value for int (0) will be returned.

Accessing nested defaultdict elements

Accessing elements in a nested defaultdict is similar to accessing elements in a regular dictionary. We can use square brackets notation to access the values at a particular key. If the key does not exist, the nested defaultdict will create a new default dictionary to store the values. The following code snippet illustrates this:

```
from collections import defaultdict

d = defaultdict(lambda: defaultdict(int))

d['a']['b'] = 1
d['a']['c'] = 2
d['d']['e'] = 3

print(d['a'])  # Output: defaultdict(<class 'int'>, {'b': 1, 'c': 2})
print(d['a']['b'])  # Output: 1
print(d['d']['f'])  # Output: 0 (default value for int)
```

In this example, we first print the entire dictionary corresponding to the key 'a'. The output is a new nested defaultdict object with keys 'b' and 'c' and corresponding values 1 and 2, respectively. We then access the value at nested key 'b' by calling d['a']['b'] and printing it. Finally, we try to access a nonexistent key 'f' in the dictionary corresponding to key 'd'. The defaultdict will create a new integer dictionary for key 'd' and then return the default value of 0 for nonexistent key 'f'.

Conclusion

In conclusion, a nested defaultdict in Python is a powerful data structure for storing and accessing complex data. It allows us to create and access nested dictionaries with ease, without having to worry about KeyError exceptions. We can also set default factory functions to customize the behavior of the nested defaultdict.
