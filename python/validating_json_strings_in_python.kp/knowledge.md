---
title: What is the method to verify if a string is in proper JSON format using python?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: Use the `json.loads` function and wrap it in a try-except block to catch any `JSONDecodeError` exceptions.
---

**Contents**

[TOC]

Using `json` module

```python
import json

def is_valid_json(json_string):
    try:
        json.loads(json_string)
        return True
    except ValueError:
        return False
```

Explanation:
- The `json.loads()` method is used to parse a JSON string, and if it fails due to invalid JSON syntax, it raises a `ValueError` exception.
- The `is_valid_json()` function tries to parse the `json_string` argument using the `json.loads()` method, and returns `True` if parsing is successful, otherwise `False`. 

Using `jsonschema` module

```python
import jsonschema

def is_valid_json(json_string):
    try:
        jsonschema.validate(json.loads(json_string), {})
        return True
    except jsonschema.exceptions.ValidationError:
        return False
```

Explanation:
- The `jsonschema` module is used to validate JSON against a JSON schema.
- In this code, we are using an empty JSON schema `{}` to validate the JSON string, which means that any valid JSON will pass the validation.
- The `jsonschema.validate()` method raises a `jsonschema.exceptions.ValidationError` exception if the JSON fails validation.

Using `re` module

```python
import re

def is_valid_json(json_string):
    pattern = r'^\s*(\{|\[)(.|\n)*(\}|\])\s*$'
    return bool(re.match(pattern, json_string))
```

Explanation:
- This method uses a regular expression to check whether the input string is valid JSON or not.
- The regular expression pattern matches JSON strings that start with either a `{` or a `[`, followed by any characters or whitespace, and end with either a `}` or a `]`.
- The `re.match()` function returns a match object if the pattern matches the string, otherwise it returns `None`.
- By using the `bool()` function, we can convert the match object to a boolean value (`True` if there is a match, otherwise `False`). 

Using `ast` module

```python
import ast

def is_valid_json(json_string):
    try:
        ast.literal_eval(json_string)
        return True
    except ValueError:
        return False
```

Explanation:
- The `ast.literal_eval()` method is used to safely evaluate a string containing a literal Python expression, and if it fails due to invalid syntax, it raises a `ValueError` exception.
- In this code, we are trying to evaluate the `json_string` argument using the `ast.literal_eval()` method, which works for JSON strings because they are valid Python expressions.
- If the evaluation is successful, the function returns `True`, otherwise `False`.
