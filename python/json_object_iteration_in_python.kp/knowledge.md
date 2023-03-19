---
title: Iterating over a JSON object
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-13 00:00:00
updated_at: 2023-03-13 00:00:00
tldr: Use a for loop to iterate through the keys and values of a JSON object in Python.
---

**Contents**

[TOC]

Section 1: Understanding JSON format
- Before iterating through a JSON object in Python, it is important to understand the format of JSON. JSON stands for JavaScript Object Notation and is a lightweight format for storing and exchanging data. It is easy for humans to read and write and easy for machines to parse and generate.
- JSON data is represented as key-value pairs, similar to dictionaries in Python. In JSON, the key is always a string, and the value can be a string, number, boolean, null, array, or another JSON object.

Section 2: Parsing JSON data in Python
- To work with JSON data in Python, we first need to parse it using the built-in json module. We can use the `json.loads()` method to load a JSON string into a Python object.
- For example, let's say we have the following JSON data:
```
{
  "name": "John Doe",
  "age": 35,
  "email": "john.doe@example.com",
  "hobbies": ["reading", "swimming", "traveling"]
}
```
We can parse it in Python as follows:
```
import json

json_data = '{"name": "John Doe", "age": 35, "email": "john.doe@example.com", "hobbies": ["reading", "swimming", "traveling"]}'
python_data = json.loads(json_data)
```
Now, `python_data` is a Python dictionary that we can work with.

Section 3: Iterating through a JSON object in Python
- Once we have parsed the JSON data into a Python object, we can iterate through it using a for loop. If the value associated with a key is another JSON object, we can use another for loop to iterate through its key-value pairs.
- For example, let's say we want to print out the name, age, and all hobbies of the person from the previous example. We can do it as follows:
```
import json

json_data = '{"name": "John Doe", "age": 35, "email": "john.doe@example.com", "hobbies": ["reading", "swimming", "traveling"]}'
python_data = json.loads(json_data)

print("Name:", python_data['name'])
print("Age:", python_data['age'])
print("Hobbies:")
for hobby in python_data['hobbies']:
    print("- " + hobby)
```
This will output:
```
Name: John Doe
Age: 35
Hobbies:
- reading
- swimming
- traveling
```

Section 4: Converting a Python object to JSON
- If we want to convert a Python object back to JSON, we can use the `json.dumps()` method. This method takes a Python object and returns a JSON formatted string.
- For example, let's say we have a Python dictionary representing a person and we want to convert it to JSON:
```
import json

person = {
  "name": "John Doe",
  "age": 35,
  "email": "john.doe@example.com",
  "hobbies": ["reading", "swimming", "traveling"]
}

json_data = json.dumps(person)
print(json_data)
```
This will output:
```
{"name": "John Doe", "age": 35, "email": "john.doe@example.com", "hobbies": ["reading", "swimming", "traveling"]}
```
