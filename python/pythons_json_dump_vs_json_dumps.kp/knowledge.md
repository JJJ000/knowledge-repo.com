---
title: How does json.dump() differ from json.dumps() in python?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-08 00:00:00
updated_at: 2023-03-08 00:00:00
tldr: json.dump() writes a Python object into a file-like object using JSON format, while json.dumps() returns a string representation of a Python object in JSON format.
---

**Contents**

[TOC]

# Introduction

The JSON module in Python provides two methods that allow us to write Python objects to JSON files or strings: `json.dump()` and `json.dumps()`. Although both methods are used to encode Python objects as JSON-formatted strings, they behave differently in terms of their output and how they handle the input. In this article, we will explore the differences between these two methods.

# json.dump()

The `json.dump()` method takes a Python object, such as a dictionary or a list, and writes the corresponding JSON-formatted string to a file-like object, such as a file stream. This means that we can use the method to encode and save data to a file in JSON format. Here is an example of how to use the `json.dump()` method:

```python
import json

data = {
    "name": "John",
    "age": 30,
    "city": "New York"
}

with open("data.json", "w") as f:
    json.dump(data, f)
```

In this example, we create a dictionary `data` that represents a person's name, age and city, and then use the `with` statement to open a file `data.json` in write mode. We pass the `data` dictionary and the file stream `f` to the `json.dump()` method which encodes `data` as a JSON-formatted string and writes it to the file. Note that the `json.dump()` method does not return anything.

# json.dumps()

The `json.dumps()` method is similar to `json.dump()` in that it also encodes a Python object as a JSON-formatted string. However, instead of writing the string to a file, the method returns the string as the output. This means that we can use the method to encode and obtain the JSON-formatted string. Here is an example of how to use the `json.dumps()` method:

```python
import json

data = {
    "name": "John",
    "age": 30,
    "city": "New York"
}

json_string = json.dumps(data)
print(json_string)
```

In this example, we create a dictionary `data` that represents a person's name, age and city. We then pass `data` to the `json.dumps()` method which encodes it as a JSON-formatted string and returns the string. We store the returned string in the variable `json_string` and then print it to the console.

# Differences between json.dump() and json.dumps()

The main differences between `json.dump()` and `json.dumps()` are:

1. Output format: The `json.dump()` method writes the JSON-formatted string to a file-like object, whereas `json.dumps()` returns the string as the output.
2. Return value: The `json.dump()` method does not return anything, whereas `json.dumps()` returns the JSON-formatted string.
3. Usage: `json.dump()` is typically used when we want to save the encoded data to a file, whereas `json.dumps()` is typically used when we want to obtain the encoded data as a string to pass it to another function or to print it to the console.

# Conclusion

In summary, the JSON module in Python provides two methods that allow us to encode Python objects as JSON-formatted strings: `json.dump()` and `json.dumps()`. These methods behave differently in terms of their output and how they handle the input. The `json.dump()` method is used to encode data and write it to a file, whereas `json.dumps()` is used to obtain the encoded data as a string. By understanding the differences between these methods, we can choose the one that best suits our needs when working with JSON data.
