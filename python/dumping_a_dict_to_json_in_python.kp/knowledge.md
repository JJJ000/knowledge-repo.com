---
title: What is the process for exporting a dictionary to a JSON file?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Use the json.dump() method to dump a dict to a JSON file in Python.
---

**Contents**

[TOC]

### 1. Import JSON Library

The first step is to import the `json` library.

```python
import json
```

### 2. Dump the Dictionary

The `json.dump()` method is used to dump a dictionary to a JSON file.

```python
# Create a dictionary
data = {
    'name': 'John Doe',
    'age': 25,
    'city': 'New York'
}

# Open a JSON file
with open('data.json', 'w') as f:
    # Dump the dictionary to the file
    json.dump(data, f)
```

### 3. Read the JSON File

The JSON file can be read using the `json.load()` method.

```python
# Open the JSON file
with open('data.json', 'r') as f:
    # Load the data from the file
    data = json.load(f)

# Print the data
print(data)
```

### 4. Output

The output will be a dictionary with the data from the JSON file.

```
{'name': 'John Doe', 'age': 25, 'city': 'New York'}
```
