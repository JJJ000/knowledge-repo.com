---
title: What is the most efficient way to read multiple JSON values from a file/stream in Python without expending much effort?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-10 00:00:00
updated_at: 2023-02-10 00:00:00
tldr: You can use the json.loads() method to lazily read multiple JSON values from a file/stream.
---

**Contents**

[TOC]

1. Using the `json` Module

The `json` module provides a `load` and `loads` functions to read JSON data from a file or stream. The `load` function takes a file-like object, while the `loads` function takes a string. 

```python
import json

# Read JSON from a file
with open('data.json', 'r') as f:
    data = json.load(f)

# Read JSON from a stream
stream = '[{"name": "John"}, {"name": "Jane"}]'
data = json.loads(stream)
```

2. Using the `ijson` Module

The `ijson` module provides an iterator-based parser for JSON data. It is designed to be used for streaming data and supports lazy parsing. To read multiple values from a file or stream, use the `items` function.

```python
import ijson

# Read JSON from a file
with open('data.json', 'r') as f:
    for item in ijson.items(f, 'name'):
        print(item)

# Read JSON from a stream
stream = '[{"name": "John"}, {"name": "Jane"}]'
for item in ijson.items(stream, 'name'):
    print(item)
```

3. Using the `ujson` Module

The `ujson` module provides an ultra fast JSON encoder and decoder written in C. It provides the same functions as the `json` module, with the addition of the `load` and `loads` functions.

```python
import ujson

# Read JSON from a file
with open('data.json', 'r') as f:
    data = ujson.load(f)

# Read JSON from a stream
stream = '[{"name": "John"}, {"name": "Jane"}]'
data = ujson.loads(stream)
```

4. Using the `rapidjson` Module

The `rapidjson` module provides a fast JSON encoder and decoder written in C++. It provides the same functions as the `json` module, with the addition of the `load` and `loads` functions.

```python
import rapidjson

# Read JSON from a file
with open('data.json', 'r') as f:
    data = rapidjson.load(f)

# Read JSON from a stream
stream = '[{"name": "John"}, {"name": "Jane"}]'
data = rapidjson.loads(stream)
```
