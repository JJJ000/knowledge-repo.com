---
title: What is the process for verifying if a string is a valid JSON object in python?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-08 00:00:00
updated_at: 2023-02-08 00:00:00
tldr: You can use the json.loads() function to check if a string is valid JSON in Python.
---

**Contents**

[TOC]

### Using the json Module

The json module can be used to check if a string is valid JSON in Python. To do this, you can use the `json.loads()` method, which will return a Python object if the string is valid JSON, or throw an exception if the string is not valid JSON.

For example:

```python
import json

json_string = '{"name": "John", "age": 30}'

try:
    json_object = json.loads(json_string)
    print("Valid JSON")
except Exception as e:
    print("Invalid JSON")
```

### Using the pprint Module

The pprint module can also be used to check if a string is valid JSON in Python. To do this, you can use the `pprint.pprint()` method, which will print the string if it is valid JSON, or throw an exception if the string is not valid JSON.

For example:

```python
import pprint

json_string = '{"name": "John", "age": 30}'

try:
    pprint.pprint(json_string)
    print("Valid JSON")
except Exception as e:
    print("Invalid JSON")
```

### Using Regular Expressions

Regular expressions can also be used to check if a string is valid JSON in Python. To do this, you can use the `re.match()` method, which will return a match object if the string is valid JSON, or raise an exception if the string is not valid JSON.

For example:

```python
import re

json_string = '{"name": "John", "age": 30}'

try:
    match = re.match(r"^\{.*\}$", json_string)
    if match:
        print("Valid JSON")
except Exception as e:
    print("Invalid JSON")
```
