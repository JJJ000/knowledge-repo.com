---
title: Retrieving and interpreting a file with multiple JSON components
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-10 00:00:00
updated_at: 2023-02-10 00:00:00
tldr: You can use a JSON parser to load and parse a JSON file with multiple JSON objects.
---

**Contents**

[TOC]

### Section 1: Loading the JSON File

To load a JSON file with multiple JSON objects, we can use the `json.load()` method. This method takes an argument of the file path and returns a Python dictionary. 

```python
import json

with open('file_path.json') as f:
    data = json.load(f)
```

### Section 2: Parsing the JSON Objects

Once the file is loaded, we can use the `json.loads()` method to parse each individual JSON object. This method takes a string argument and returns a Python dictionary. 

```python
for obj in data:
    parsed_obj = json.loads(obj)
```

### Section 3: Accessing the Data

Once the JSON objects are parsed, we can access the data within each object using the standard dictionary syntax. 

```python
for obj in data:
    parsed_obj = json.loads(obj)
    print(parsed_obj['key'])
```

### Section 4: Iterating Through Multiple JSON Objects

We can also iterate through multiple JSON objects by looping through the data list. 

```python
for obj in data:
    parsed_obj = json.loads(obj)
    for key, value in parsed_obj.items():
        print(key, value)
```
