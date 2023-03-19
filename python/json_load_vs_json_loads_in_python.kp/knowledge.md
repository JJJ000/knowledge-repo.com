---
title: How do the functions json.load() and json.loads() differ from each other?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-05 00:00:00
updated_at: 2023-03-05 00:00:00
tldr: json.load() function reads JSON data from a file, while json.loads() function reads JSON data from a string.
---

**Contents**

[TOC]

# Explanation

Both `json.load()` and `json.loads()` are functions provided by the Python `json` module for handling JSON data. However, there is a key difference between the two functions.

## json.load()

`json.load()` reads a JSON file object from a file and returns a deserialized JSON object as a Python object. 

Here's an example:

```python
import json

with open('data.json') as f:
    data = json.load(f)
```

In this example, `data.json` is a JSON file in the current directory.

## json.loads()

`json.loads()` deserializes a string containing a JSON object and returns a Python object.

Here's an example:

```python
import json

data = '{"name": "John", "age": 30, "city": "New York"}'
json.loads(data)
```

In this example, `data` is a JSON string, and `json.loads(data)` returns a Python object representing the JSON data. 

## Key difference

The key difference between `json.load()` and `json.loads()` is that `json.load()` reads a JSON file object from a file, while `json.loads()` deserializes a JSON string.

If you have a JSON file on disk, you would use `json.load()`, and if you have a JSON string in memory, you would use `json.loads()`.
