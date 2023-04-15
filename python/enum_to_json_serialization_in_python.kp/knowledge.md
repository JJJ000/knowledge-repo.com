---
title: Transforming an enumeration element into JSON format
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Use the `json.dumps()` function with the `default` parameter set to `lambda o o.value` to serialise an Enum member to JSON in Python.
---

**Contents**

[TOC]

## Introduction
Enums or enumeration classes in Python are a powerful feature that lets developers define a set of symbolic names that map to unique values. They're useful for defining groups of related constants, especially when those constants are used in multiple places throughout a project. When working with JSON data, it's often necessary to serialize enum members to JSON. In this tutorial, we'll look at how to do that in Python.

## Step 1: Importing the necessary library
We'll be using the `json` library in Python to serialize enum members to JSON. This is a built-in library, so no installation is necessary. Simply import it as follows:

```python
import json
```

## Step 2: Creating our enum class
For this example, we'll create an enum class with a few members:

```python
from enum import Enum

class Color(Enum):
    RED = 1
    GREEN = 2
    BLUE = 3
```

## Step 3: Serializing an enum member to JSON
Now let's say we want to serialize the `GREEN` member of our `Color` enum to JSON. We can do this using the `json.dumps()` function, which takes a Python object and returns its JSON representation:

```python
green_json = json.dumps(Color.GREEN.value)
```

Here, we're calling the `value` attribute of the `GREEN` member to get its value, which is then passed to the `dumps()` function.

## Step 4: Checking the output
Let's print `green_json` to see the output:

```python
print(green_json)
```

The output should be:

```json
"2"
```

This is the JSON representation of the `GREEN` member of our `Color` enum.

## Conclusion
Serializing enum members to JSON in Python is a simple process. By using the `json` library and accessing the `value` attribute of enum members, we can easily serialize our Python objects to JSON. This can be useful when working with APIs or other systems that require JSON input.
