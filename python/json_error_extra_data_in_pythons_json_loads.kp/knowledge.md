---
title: The valueerror extra data error is displayed by json.loads in python
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-17 00:00:00
updated_at: 2023-04-17 00:00:00
tldr: It means that the JSON string being parsed contains more than one JSON object, which is not valid.
---

**Contents**

[TOC]

Section 1: Introduction
Python provides JSON (JavaScript Object Notation) utility functions to parse and generate JSON. In Python, json.load() and json.loads() can parse JSON data into Python objects.

Section 2: ValueError: Extra data
If you encounter an error 'ValueError: Extra data' while using json.loads() in Python, it means that the input string has multiple JSON objects instead of a single one. The JSON specification only allows one object to be represented in a JSON string. Thus, when json.loads() tries to parse it, it finds multiple objects and raises an error.

Section 3: Example
Let's consider an example where multiple JSON objects are provided in a single string and we try to parse it using json.loads().

``` python
import json

data = '''
{
    "name": "John",
    "age": 30
}
{
    "name": "Jane",
    "age": 25
}
'''

jsonData = json.loads(data)
```

Output:
```
ValueError: Extra data
```

Section 4: Solution
To fix the error, we need to ensure that the JSON string contains only one object. We can do this by either providing a single JSON object or an array of JSON objects. For example, we can modify the data string in the example like this.

``` python
import json

data = '''
[
    {
        "name": "John",
        "age": 30
    },
    {
        "name": "Jane",
        "age": 25
    }
]
'''

jsonData = json.loads(data)
```

Now, the json.loads() command will work correctly and parse the JSON data into Python objects without raising the ValueError.
