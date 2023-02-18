---
title: Transform a JSON string into a Python object
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-18 00:00:00
updated_at: 2023-02-18 00:00:00
tldr: Use the json.loads() method to convert a JSON string to a Python object.
---

**Contents**

[TOC]

## Using the json Module

The json module can be used to convert a JSON string to a Python object. To do this, the json.loads() method is used to convert a JSON string to a Python dictionary.

```
import json

json_string = '{"name": "John Smith", "age": 30}'

python_obj = json.loads(json_string)

print(python_obj)
```

Output: 
```
{'name': 'John Smith', 'age': 30}
```

## Using the ast Module

The ast module can also be used to convert a JSON string to a Python object. The ast.literal_eval() method is used to evaluate a string containing a Python literal or container display.

```
import ast

json_string = '{"name": "John Smith", "age": 30}'

python_obj = ast.literal_eval(json_string)

print(python_obj)
```

Output: 
```
{'name': 'John Smith', 'age': 30}
```
