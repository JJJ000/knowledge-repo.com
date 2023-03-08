---
title: Using python, save JSON data to a file in a readable format
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-08 00:00:00
updated_at: 2023-03-08 00:00:00
tldr: The code below can be used to pretty-print JSON data to a file in Python

```
import json

with open(`output.json`, `w`) as outfile
    json.dump(data, outfile, indent=4)
```

(where `data` is your JSON data to be printed)
---

**Contents**

[TOC]

Parsing JSON Data
------------------
Before printing JSON data in a pretty format, it needs to be parsed. This can be done using Python's built-in `json` module. The `json` module provides two methods for parsing JSON data: `loads()` and `load()`.

- `loads()` is used to parse JSON data that is stored as a string.
- `load()` is used to parse JSON data that is stored in a file.

Here is an example of using `load()` to parse JSON from a file:

```python
import json

with open('data.json', 'r') as f:
    data = json.load(f)
```

The `data` variable now contains the parsed JSON data.


Printing JSON Data to a File
---------------------------
Once the JSON data has been parsed, it can be pretty-printed to a file using the `json.dump()` method. The `dump()` method takes three parameters: the data to be dumped, the file to be written to, and an optional `indent` parameter to specify the number of spaces to use for indentation.

Here is an example of using `dump()` to pretty-print the parsed JSON data to a file:

```python
import json

with open('data.json', 'r') as f:
    data = json.load(f)

with open('output.json', 'w') as f:
    json.dump(data, f, indent=4)
```

This will write the pretty-printed JSON to a file named `output.json`.


Complete Example
----------------
Here is a complete example that demonstrates how to parse JSON from a file and pretty-print it to another file:

```python
import json

with open('data.json', 'r') as f:
    data = json.load(f)

with open('output.json', 'w') as f:
    json.dump(data, f, indent=4)
```

This will read the JSON data from a file named `data.json`, parse it, and then write the pretty-printed JSON to a file named `output.json`, using an indentation of 4 spaces.
