---
title: Changing a dictionary into a JSON file
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-01 00:00:00
updated_at: 2023-02-01 00:00:00
tldr: You can convert a dictionary to JSON in Python by using the json.dumps() method.
---

**Contents**

[TOC]

# Section 1: What is JSON?

JSON (JavaScript Object Notation) is a lightweight data-interchange format. It is based on a subset of the JavaScript Programming Language, Standard ECMA-262 3rd Edition - December 1999. JSON is a text format that is language independent, but uses conventions that are familiar to programmers of the C-family of languages, including C, C++, C#, Java, JavaScript, Perl, Python, and many others. These properties make JSON an ideal data-interchange language.

# Section 2: What is a Dictionary?

A dictionary is a collection of key-value pairs. In Python, dictionaries are written with curly brackets, and they have keys and values separated by a colon. Each key is separated from its value by a comma, and the whole dictionary is enclosed within curly brackets. The keys in a Python dictionary must be immutable objects like strings or numbers. The values in a dictionary can be any data type, such as strings, lists, or other dictionaries.

# Section 3: Converting a Dictionary to JSON

Converting a dictionary to JSON is fairly straightforward in Python. The json.dumps() method takes a Python dictionary and returns a JSON string. The json.dumps() method has parameters that allow you to format and customize the output. For example, you can sort the keys in the result, or add whitespace to make it more readable.

# Section 4: Example

Let's look at an example of how to convert a dictionary to JSON in Python.

```python
import json

# Create a dictionary
my_dict = {
  "name": "John",
  "age": 30,
  "city": "New York"
}

# Convert the dictionary to JSON
my_json = json.dumps(my_dict)

# Print the JSON
print(my_json)
```

Output:

```json
{"name": "John", "age": 30, "city": "New York"}
```
