---
title: Converting a list of dictionaries to JSON format using python
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-10 00:00:00
updated_at: 2023-02-10 00:00:00
tldr: Use the json.dumps() method to convert a list of dictionaries to JSON.
---

**Contents**

[TOC]

##### Step 1: Create a List of Dictionaries

To convert a list of dictionaries to JSON, we must first create a list of dictionaries. A dictionary is a collection of key-value pairs. Here is an example of a dictionary:

```python
my_dict = {
    'name': 'John',
    'age': 32,
    'city': 'New York'
}
```

We can create a list of dictionaries by adding multiple dictionaries to a list. Here is an example of a list of dictionaries:

```python
my_list = [
    {
        'name': 'John',
        'age': 32,
        'city': 'New York'
    },
    {
        'name': 'Jane',
        'age': 28,
        'city': 'Los Angeles'
    },
    {
        'name': 'Bob',
        'age': 41,
        'city': 'Chicago'
    }
]
```

##### Step 2: Import the JSON Module

In order to convert a list of dictionaries to JSON, we must first import the JSON module. This module provides us with the necessary functions to convert a list of dictionaries to JSON.

```python
import json
```

##### Step 3: Convert the List of Dictionaries to JSON

Now that we have imported the JSON module, we can use the `json.dumps()` function to convert the list of dictionaries to JSON. The `json.dumps()` function takes the list of dictionaries as an argument and returns a JSON string.

```python
my_json = json.dumps(my_list)
```

##### Step 4: Print the JSON String

Finally, we can print the JSON string to see the result.

```python
print(my_json)
```

The result should be a JSON string that looks like this:

```json
[{"name": "John", "age": 32, "city": "New York"}, {"name": "Jane", "age": 28, "city": "Los Angeles"}, {"name": "Bob", "age": 41, "city": "Chicago"}]
```
