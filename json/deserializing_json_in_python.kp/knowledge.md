---
title: Convert a JSON string into a Python object using deserialization
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-10 00:00:00
updated_at: 2023-02-10 00:00:00
tldr: Use the json.loads() function to deserialize a JSON string to an object in Python.
---

**Contents**

[TOC]

### Deserializing JSON

Deserializing JSON is the process of converting a JSON string into a Python object. The JSON string must be valid and correctly formatted in order for the deserialization process to be successful.

### Using the json Module

The json module is a built-in Python library that allows for the deserialization of JSON strings. The json.loads() method is used to deserialize a JSON string. This method takes a single argument, which is the JSON string to be deserialized.

### Example

The following example shows how to deserialize a JSON string using the json module.

```python
import json

json_string = '{"name": "John Smith", "age": 30}'

# Deserialize the JSON string
data = json.loads(json_string)

# Print out the deserialized data
print(data)

# Output: {'name': 'John Smith', 'age': 30}
```

### Using the ast Module

The ast module is another built-in Python library that can be used to deserialize JSON strings. The ast.literal_eval() method is used to deserialize a JSON string. This method takes a single argument, which is the JSON string to be deserialized.

### Example

The following example shows how to deserialize a JSON string using the ast module.

```python
import ast

json_string = '{"name": "John Smith", "age": 30}'

# Deserialize the JSON string
data = ast.literal_eval(json_string)

# Print out the deserialized data
print(data)

# Output: {'name': 'John Smith', 'age': 30}
```
