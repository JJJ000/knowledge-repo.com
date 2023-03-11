---
title: The JSON module of Python transforms integer dictionary keys into strings
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-11 00:00:00
updated_at: 2023-03-11 00:00:00
tldr: Yes, Python`s JSON module converts int dictionary keys to strings.
---

**Contents**

[TOC]

Introduction

JSON (JavaScript Object Notation) is a lightweight format used for data exchange between applications. Python has a built-in module called `json` that can be used for serializing and deserializing JSON data. When using the `json` module, if the dictionary has int keys, they will be automatically converted to strings by default. In this article, we will explain why this happens and how to prevent it.

Why Int Keys are Converted to Strings

When a dictionary is serialized to JSON in Python, the serializer (json.dumps) checks the type of the dictionary keys. If they are not strings, they will be automatically converted to strings. This is because the JSON format only supports string keys.

For example, consider the following dictionary:

```python
data = {1: 'one', 2: 'two', 3: 'three'}
```

If we serialize this dictionary to JSON, we get the following output:

```python
import json

json.dumps(data)
# Output: '{"1": "one", "2": "two", "3": "three"}'
```

As you can see, the int keys have been converted to strings in the JSON output.

How to Prevent Int Keys from Being Converted to Strings

If you want to prevent int keys from being converted to strings when serializing a dictionary in Python, you can use the `ensure_ascii` parameter of the json.dumps() method. This parameter tells the serializer to encode all non-ASCII characters in the input data as Unicode escape sequences. By default, `ensure_ascii` is set to `True`, which means that all non-ASCII characters will be escaped in the output.

Here's an example:

```python
data = {1: 'one', 2: 'two', 3: 'three'}

json.dumps(data, ensure_ascii=False)
# Output: '{"1": "one", "2": "two", "3": "three"}'
```

In this example, we have set the `ensure_ascii` parameter to `False` to prevent the int keys from being converted to strings in the output.

Conclusion

Python's json module automatically converts dictionary int keys to strings when serializing to JSON by default. This is because the JSON format only supports string keys. However, we can prevent int keys from being converted to strings by setting the ensure_ascii parameter to False when serializing the dictionary using json.dumps().
