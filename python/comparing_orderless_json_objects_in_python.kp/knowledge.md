---
title: How can two JSON objects with identical elements but arranged differently be compared and considered equal?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: One way to compare two JSON objects with the same elements in a different order equal in Python is to convert them into sets and compare them.
---

**Contents**

[TOC]

## Getting Started

In Python, JSON objects can be compared easily using the `json` module's `loads` function to parse the JSON strings into Python dictionaries, followed by the `assert` function to compare the resulting dictionaries. However, if the JSON objects have the same elements but in a different order, they will not be considered equal using the default comparison method. In this guide, we will explore how to compare such JSON objects as equal by reordering the elements before comparison.


## Sorting the JSON Objects

To compare two JSON objects that have the same elements but in a different order, we must first sort the elements of each object before comparison. We can achieve this by loading the JSON strings into Python dictionaries, sorting the dictionaries by their keys, and then converting them back to JSON strings. Here's the code to do that:

```python
import json

def sort_json(json_str):
    obj = json.loads(json_str)
    sorted_obj = dict(sorted(obj.items()))
    return json.dumps(sorted_obj)

json_str1 = '{"name": "Peter", "age": 34, "city": "New York"}'
json_str2 = '{"city": "New York", "age": 34, "name": "Peter"}'

assert sort_json(json_str1) == sort_json(json_str2)
```

In this code snippet, the `sort_json` function takes a JSON string as input, loads it into a Python dictionary, sorts the dictionary by its keys, and then converts it back to a JSON string. The assertion statement at the end confirms that the two JSON objects are equal after sorting their elements.


## Comparing the Sorted JSON Objects

With the elements of the JSON objects sorted, we can now compare them using the default `assert` function or any custom comparison function. Here's how to use the `sort_json` function to compare two JSON objects:

```python
import json

def sort_json(json_str):
    obj = json.loads(json_str)
    sorted_obj = dict(sorted(obj.items()))
    return json.dumps(sorted_obj)

json_str1 = '{"name": "Peter", "age": 34, "city": "New York"}'
json_str2 = '{"city": "New York", "age": 34, "name": "Peter"}'

assert sort_json(json_str1) == sort_json(json_str2)
```

In this example, we first sort the elements of the two JSON objects using the `sort_json` function and then use the `assert` function to compare them. If the two objects are equal, the assertion passes; otherwise, it raises an error.


## Conclusion

Comparing two JSON objects with the same elements but in a different order can be challenging, but it can be done by sorting the elements before comparison. We've shown how to accomplish this using the `json` module in Python, and we hope this guide has been helpful. By following these steps, you can easily compare any JSON objects, regardless of element order.
