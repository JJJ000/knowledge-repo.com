---
title: Transform a bytes array to JSON notation
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-16 00:00:00
updated_at: 2023-04-16 00:00:00
tldr: To convert a bytes array into JSON format in Python, we can use the decode method with UTF-8 encoding on the bytes object and then pass it to the loads method of the JSON module.
---

**Contents**

[TOC]

## Introduction
In Python, we can use the `json` module to convert a bytes array into a JSON format. We can use the `loads()` function to load the bytes array into a JSON format.

## Example
Here's an example of how we can convert a bytes array into a JSON format:

```python
import json

# creating a bytes array
bytes_val = b'{"name": "John","age": 30,"city": "New York"}'

# converting bytes array to JSON format
json_val = json.loads(bytes_val)

# printing JSON format
print(json_val)
```

In this example, we create a bytes array using the `b` prefix. We then use the `json.loads()` function to convert the bytes array to a JSON format. Finally, we print the JSON format using the `print()` function. 

## Explanation
The `json.loads()` function deserializes a string containing a JSON document to a Python object. In our example, we pass a bytes array to this function, and it returns a Python object representing the JSON document.

## Conclusion
We can convert a bytes array into a JSON format in Python using the `json` module's `loads()` function. The `loads()` function deserializes a string containing a JSON document to a Python object.
