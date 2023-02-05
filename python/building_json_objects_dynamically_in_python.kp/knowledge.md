---
title: What is the process for constructing a JSON object dynamically?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: Use a dictionary to dynamically build a JSON object in Python.
---

**Contents**

[TOC]

#### Using Dictionary

We can use a dictionary to dynamically build a JSON object in Python. A dictionary is a collection which is unordered, changeable and indexed. In Python, dictionaries are written with curly brackets, and they have keys and values.

```python
# Create an empty dictionary
my_dict = {}

# Add key-value pairs
my_dict['name'] = 'John'
my_dict['age'] = 25
my_dict['city'] = 'New York'

# Print the dictionary
print(my_dict)
```

#### Using json.dumps()

The json.dumps() function can be used to convert a Python dictionary to a JSON string.

```python
# Create a dictionary
my_dict = {
  'name': 'John',
  'age': 25,
  'city': 'New York'
}

# Convert the dictionary to JSON string
json_str = json.dumps(my_dict)

# Print the JSON string
print(json_str)
```

#### Using json.loads()

The json.loads() function can be used to convert a JSON string to a Python dictionary.

```python
# Create a JSON string
json_str = '{"name": "John", "age": 25, "city": "New York"}'

# Convert the JSON string to a dictionary
my_dict = json.loads(json_str)

# Print the dictionary
print(my_dict)
```

#### Using json.dump()

The json.dump() function can be used to write a Python dictionary to a JSON file.

```python
# Create a dictionary
my_dict = {
  'name': 'John',
  'age': 25,
  'city': 'New York'
}

# Open a JSON file
with open('data.json', 'w') as f:
  # Write the dictionary to the file
  json.dump(my_dict, f)
```
