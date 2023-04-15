---
title: Reworded compress keys by flattening dictionaries that are nested
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: You can use a recursive function with a loop to flatten a nested dictionary and compress the keys by joining them with a separator.
---

**Contents**

[TOC]

## Introduction

In some situations, we may have to work with a deeply nested dictionary with numerous keys and subkeys. It becomes very difficult to handle such nested dictionaries in Python programming, which may lead to decreased performance and slower code execution. In this case, we can use the `flatten` function in Python to convert the nested dictionary into a flat dictionary by compressing the keys.

## Understanding nested dictionaries

Before we discuss the process to flatten nested dictionaries, let's first understand what nested dictionaries are.

In Python, a nested dictionary is a dictionary inside another dictionary. It is a collection of key-value pairs in which the values of a dictionary can be other dictionaries, lists, or even other complex data structures.

Here is an example of a nested dictionary:

```
nested_dict = {
    'a': {
        'b': {
            'c': 1
        }
    },
    'd': [2, 3, 4]
}
```

## Flattening nested dictionaries

Flattening a nested dictionary means converting it into a flat dictionary by compressing the keys. This process of flattening will create a flat dictionary where each key will be the compressed version of nested keys.

Let's consider the same nested dictionary used in the previous section:

```
nested_dict = {
    'a': {
        'b': {
            'c': 1
        }
    },
    'd': [2, 3, 4]
}
````

After flattening, the dictionary should look like this:

```
flat_dict = {
    'a.b.c': 1,
    'd': [2, 3, 4]
}
```

## Using the `flatten` function

In Python, we can flatten a nested dictionary using the `flatten` function provided by the library `flatten_dict`. 

The `flatten` function takes the nested dictionary as input and returns a flattened dictionary as output. Here's how you can use it:

```python
from flatten_dict import flatten

nested_dict = {
    'a': {
        'b': {
            'c': 1
        }
    },
    'd': [2, 3, 4]
}

flat_dict = flatten(nested_dict)

print(flat_dict)
```

Output:

```
{
    'a.b.c': 1,
    'd': [2, 3, 4]
}
```

## Conclusion

Flattening a nested dictionary is very useful when we have to handle a large amount of data in Python. It can help to simplify the code and improve its performance. In this article, we discussed the basic concepts of nested dictionaries and how to flatten them using the `flatten` function.
