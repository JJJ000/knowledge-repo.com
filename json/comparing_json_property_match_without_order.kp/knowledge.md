---
title: What is the method to check if two JSON objects have identical properties regardless of their sequence?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Convert the JSONs to dictionaries and check that they have the same key-value pairs using the set() function.
---

**Contents**

[TOC]

## Section 1: Introduction

JSON (JavaScript Object Notation) is a popular lightweight data interchange format used to transmit data between client and server. JSON objects are unordered, which means that the order of properties can vary in different JSON objects. When comparing two JSON objects that have the same properties, we need to check if the objects have the same properties regardless of their order. In this article, we will discuss how to compare two JSON objects with the same properties without considering their order.

## Section 2: Converting JSON objects to Python dictionaries

Before comparing two JSON objects, we need to convert them to Python dictionaries because Python dictionaries are easy to compare. We can use the `json` module in Python to convert JSON objects to dictionaries.

```python
import json

json_obj = '{"name": "Alice", "age": 30, "address": {"city": "New York", "state": "NY"}}'

# convert JSON object to dictionary
dict_obj = json.loads(json_obj)

print(dict_obj)
# Output: {'name': 'Alice', 'age': 30, 'address': {'city': 'New York', 'state': 'NY'}}
```

## Section 3: Comparing two JSON objects

To compare two JSON objects without considering their order, we can convert both objects to dictionaries and use the `assertDictEqual` method from the `unittest` module in Python. This method compares two dictionaries recursively, ignoring the order of keys.

```python
import json
import unittest

# JSON objects
json_obj1 = '{"name": "Alice", "age": 30, "address": {"city": "New York", "state": "NY"}}'
json_obj2 = '{"address": {"state": "NY", "city": "New York"},"name": "Alice", "age": 30}'

# convert JSON objects to dictionaries
dict_obj1 = json.loads(json_obj1)
dict_obj2 = json.loads(json_obj2)

# compare two dictionaries
class TestJsonCompare(unittest.TestCase):
  def test_json_compare(self):
    self.assertDictEqual(dict_obj1, dict_obj2)

if __name__ == '__main__':
  unittest.main()
```

In the example above, we first convert two JSON objects to dictionaries (`dict_obj1` and `dict_obj2`). Then we define a `TestJsonCompare` class that inherits from `unittest.TestCase` and defines a `test_json_compare` method that compares two dictionaries using the `assertDictEqual` method. Finally, we run the unittest using `unittest.main()`.

## Section 4: Conclusion

Comparing two JSON objects that have the same properties without considering their order is a common task in web development. By converting the JSON objects to Python dictionaries and using the `assertDictEqual` method from the `unittest` module, we can easily compare both objects and ensure that they have the same properties, regardless of their order.
