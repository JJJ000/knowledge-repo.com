---
title: What is the process for loading JSON into an ordereddict?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-02 00:00:00
updated_at: 2023-02-02 00:00:00
tldr: Yes, you can use the json.loads() function to load JSON into an OrderedDict in Python.
---

**Contents**

[TOC]

## Yes

It is possible to get JSON to load into an OrderedDict in Python. An OrderedDict is a dictionary that remembers the order of entries and allows for the efficient retrieval of keys and values. It is a subclass of the built-in dict class.

## How

The easiest way to load JSON into an OrderedDict is to use the json.loads() method, which takes a JSON string and returns a Python object. This method can be used to convert a JSON string into an OrderedDict.

## Example

For example, to convert a JSON string into an OrderedDict, you can use the following code:

```python
import json

json_string = '{"key1": "value1", "key2": "value2"}'

ordered_dict = json.loads(json_string, object_pairs_hook=OrderedDict)

print(ordered_dict)
# Output: OrderedDict([('key1', 'value1'), ('key2', 'value2')])
```

## Conclusion

In conclusion, it is possible to get JSON to load into an OrderedDict in Python. This can be done using the json.loads() method, which takes a JSON string and returns a Python object. This method can be used to convert a JSON string into an OrderedDict.
