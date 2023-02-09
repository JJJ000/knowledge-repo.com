---
title: Python - JSON with no whitespace
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-08 00:00:00
updated_at: 2023-02-08 00:00:00
tldr: Python`s json.dumps() function can be used to produce a JSON string without whitespaces.
---

**Contents**

[TOC]

# Option 1: Use json.dumps

Python's `json` module provides a `dumps` method which allows users to serialize a Python object into a JSON string. The `dumps` method takes an optional parameter, `separators`, which can be used to specify the characters used to separate objects and properties. By setting `separators` to `(',', ':')`, whitespaces can be removed from the output.

Example:

```python
import json

data = {'name': 'John', 'age': 20}

json_str = json.dumps(data, separators=(',', ':'))
print(json_str)

# Output: {"name:John,age:20"}
```

# Option 2: Use json.dump

Python's `json` module also provides a `dump` method which allows users to serialize a Python object into a JSON file. The `dump` method takes an optional parameter, `separators`, which can be used to specify the characters used to separate objects and properties. By setting `separators` to `(',', ':')`, whitespaces can be removed from the output.

Example:

```python
import json

data = {'name': 'John', 'age': 20}

with open('data.json', 'w') as f:
    json.dump(data, f, separators=(',', ':'))

# Output: {"name:John,age:20"}
```
