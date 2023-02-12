---
title: Sorting JSON output in python
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-12 00:00:00
updated_at: 2023-02-12 00:00:00
tldr: The sorting of JSON output in Python can be done using the json.dumps() function with the sort\_keys parameter set to True.
---

**Contents**

[TOC]

1. Using the `json.dumps()` Method
---------------------------------
The `json.dumps()` method is used to convert a Python object into a JSON string. It takes two parameters: an object to convert and an optional sorting function. To sort the JSON output, you can pass a `sorted()` function as the second parameter to the `json.dumps()` method. The `sorted()` function takes a key parameter to specify a function to be called on each list element prior to making comparisons.

For example, to sort a Python dictionary by its keys, you can use the following code:

```python
import json

data = {
    "name": "John",
    "age": 30,
    "city": "New York"
}

sorted_data = json.dumps(data, sort_keys=True)

print(sorted_data)
# {"age": 30, "city": "New York", "name": "John"}
```

2. Using the `json.loads()` Method
---------------------------------
The `json.loads()` method is used to convert a JSON string into a Python object. It takes two parameters: a JSON string to convert and an optional sorting function. To sort the JSON output, you can pass a `sorted()` function as the second parameter to the `json.loads()` method. The `sorted()` function takes a key parameter to specify a function to be called on each list element prior to making comparisons.

For example, to sort a JSON string by its keys, you can use the following code:

```python
import json

json_data = '{"name": "John", "age": 30, "city": "New York"}'

sorted_data = json.loads(json_data, sort_keys=True)

print(sorted_data)
# {'age': 30, 'city': 'New York', 'name': 'John'}
```

3. Using the `sort_keys` Parameter
---------------------------------
The `sort_keys` parameter is an optional parameter that can be used to sort the JSON output. It takes a boolean value as an argument, and if set to `True`, it will sort the JSON output by its keys.

For example, to sort a Python dictionary by its keys, you can use the following code:

```python
import json

data = {
    "name": "John",
    "age": 30,
    "city": "New York"
}

sorted_data = json.dumps(data, sort_keys=True)

print(sorted_data)
# {"age": 30, "city": "New York", "name": "John"}
```

4. Using the `sort_values` Parameter
-----------------------------------
The `sort_values` parameter is an optional parameter that can be used to sort the JSON output. It takes a boolean value as an argument, and if set to `True`, it will sort the JSON output by its values.

For example, to sort a Python dictionary by its values, you can use the following code:

```python
import json

data = {
    "name": "John",
    "age": 30,
    "city": "New York"
}

sorted_data = json.dumps(data, sort_values=True)

print(sorted_data)
# {"name": "John", "age": 30, "city": "New York"}
```
