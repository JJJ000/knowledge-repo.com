---
title: The error message "typeerror object of type 'int64' cannot be serialized to json" is encountered in python
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-08 00:00:00
updated_at: 2023-03-08 00:00:00
tldr: Python cannot convert an int64 data type to JSON, resulting in a Type Error.
---

**Contents**

[TOC]

# Introduction
When working with JSON serialization in Python, it's not uncommon to come across the `TypeError: Object of type 'int64' is not JSON serializable` error. This error occurs when you try to serialize an object that can't be converted to JSON format. In this article, we'll discuss the causes of this error and how to fix them.

# Causes of the Error
The `TypeError: Object of type 'int64' is not JSON serializable` error occurs when you try to serialize an object using the `json.dumps()` function and the object contains a value of type `int64`. `int64` is a data type in the NumPy library, and it can't be converted to JSON format directly. 

# Solutions to the Error
There are several ways you can fix the `TypeError: Object of type 'int64' is not JSON serializable` error, and we'll discuss two of them below.

## Solution 1: Convert int64 to int
One way to fix this error is to convert the `int64` values in your object to regular `int` values before serializing the object. You can do this using the `astype()` function in the NumPy library. Here's an example:

``` python
import numpy as np
import json

# create a NumPy array containing int64 values
arr = np.array([1, 2, 3], dtype=np.int64)

# convert the int64 values to int
arr = arr.astype(np.int)

# serialize the array to JSON format
json_arr = json.dumps(arr)

print(json_arr)
```

In this example, we created a NumPy array containing `int64` values, converted the values to regular `int` values, and then serialized the array to JSON format using the `json.dumps()` function.

## Solution 2: Use a Custom Encoder
Another way to fix this error is to write a custom encoder that can handle `int64` values. You can do this by subclassing the `json.JSONEncoder` class and overriding its `default()` method. Here's an example:

``` python
import json
import numpy as np

class NumPyEncoder(json.JSONEncoder):
    def default(self, obj):
        if isinstance(obj, np.integer):
            return int(obj)
        elif isinstance(obj, np.floating):
            return float(obj)
        elif isinstance(obj, np.ndarray):
            return obj.tolist()
        else:
            return super(NumPyEncoder, self).default(obj)

# create a NumPy array containing int64 values
arr = np.array([1, 2, 3], dtype=np.int64)

# serialize the array to JSON format using the custom encoder
json_arr = json.dumps(arr, cls=NumPyEncoder)

print(json_arr)
```

In this example, we created a custom encoder called `NumPyEncoder` that can handle `int64` values. We then used the `json.dumps()` function, passed our array and the `NumPyEncoder` class to it as arguments to serialize the array to JSON format. 

# Conclusion
The `TypeError: Object of type 'int64' is not JSON serializable` error can be fixed by either converting `int64` values to regular `int` values or by writing a custom encoder that can handle `int64` values. The solutions discussed above should help you solve this error and serialize your object in JSON format.
