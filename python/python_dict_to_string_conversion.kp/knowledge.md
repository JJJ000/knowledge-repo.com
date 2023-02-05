---
title: Change a Python dictionary into a string representation and then return it to its original form
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: You can convert a Python dict to a string using the json.dumps() method and back to a dict using the json.loads() method.
---

**Contents**

[TOC]

#### Converting a Python Dict to a String

The `json` module provides a `dumps()` method that can be used to convert a Python dictionary to a string. This method takes the dictionary as an argument and returns the string representation of the dictionary.

```python
import json

my_dict = { 'name': 'John', 'age': 30 }

dict_str = json.dumps(my_dict)

print(dict_str)
# Output: {"name": "John", "age": 30}
```

#### Converting a String to a Python Dict

The `json` module also provides a `loads()` method that can be used to convert a string to a Python dictionary. This method takes the string as an argument and returns the dictionary representation of the string.

```python
import json

dict_str = '{"name": "John", "age": 30}'

my_dict = json.loads(dict_str)

print(my_dict)
# Output: {'name': 'John', 'age': 30}
```
