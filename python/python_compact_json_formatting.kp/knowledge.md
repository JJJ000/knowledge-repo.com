---
title: How to remove whitespaces from JSON in python?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: To generate JSON without whitespaces in Python, use the `separators` parameter in the json.dumps() function.
---

**Contents**

[TOC]

Section 1: Introduction
Python is a high-level programming language that supports JSON format. JSON is a lightweight data-interchange format that stores data in key-value pairs. It is widely used for data transmission between web services and applications. The JSON format stores data in a readable format that is easy to parse and interpret. However, sometimes we need to remove the whitespaces in JSON for various reasons. In this article, we will learn how to remove whitespace in JSON using Python.

Section 2: Using the json.dumps() method
The json.dumps() method is used to serialize Python objects to a JSON string. While serializing the object, we can pass the separators parameter to remove the whitespaces in the JSON string. Here's an example:

import json

data = {'name': 'John', 'age': 30, 'city': 'New York'}

json_data = json.dumps(data, separators=(',', ':'))

print(json_data)

Output:
{"name":"John","age":30,"city":"New York"}

In the above example, we have passed the separators parameter to the json.dumps() method. The separators parameter is a tuple containing two values: the first value is the separator between the key-value pairs, and the second value is the separator between the keys and the values. Here, we have passed a comma as the separator between the key-value pairs and a colon as the separator between the keys and the values. This removes the whitespaces in the JSON string.

Section 3: Using the json.dump() method
The json.dump() method is used to serialize Python objects to a JSON file. While serializing the object, we can pass the separators parameter to remove the whitespaces in the JSON file. Here's an example:

import json

data = {'name': 'John', 'age': 30, 'city': 'New York'}

with open('data.json', 'w') as f:
    json.dump(data, f, separators=(',', ':'))

In the above example, we have opened a file named 'data.json' in write mode and passed the separators parameter to the json.dump() method. The separators parameter is the same as in the json.dumps() method. This removes the whitespaces in the JSON file.

Section 4: Conclusion
In this article, we have learned how to remove whitespaces in JSON using Python. We have seen two methods: json.dumps() and json.dump(). Both methods use the separators parameter to remove the whitespaces in JSON. This is useful when we need to reduce the size of the JSON data for transmission or storage purposes.
