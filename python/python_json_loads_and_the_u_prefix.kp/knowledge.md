---
title: The json.loads in Python produces items with 'u' prefix added
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-12 00:00:00
updated_at: 2023-03-12 00:00:00
tldr: The prefix `u` indicates that the value is a Unicode string.
---

**Contents**

[TOC]

Explanation of json.loads()

json.loads() is a method in Python that parses a JSON string and converts it into a Python dictionary or list. The JSON string can be in the form of a file or a string. This method is useful when dealing with JSON data in Python.

Example input and output

Here is an example of a JSON string:

```
import json

json_string = '{"name": "John", "age": 30, "city": "New York"}'
parsed_json = json.loads(json_string)

print(parsed_json)
```

The output of the code would be:

```
{'name': 'John', 'age': 30, 'city': 'New York'}
```

Prefixing with 'u'

In some cases, when we parse a JSON string using json.loads(), the resulting dictionary may have 'u' prefixes on some of the keys and values. For example:

```
import json

json_string = '{"name": "John", "age": 30, "city": "New York"}'
parsed_json = json.loads(json_string)

print(parsed_json)
```

Output:
```
{u'name': u'John', u'age': 30, u'city': u'New York'}
```

The presence of the 'u' prefix indicates that these keys and values are Unicode strings. Unicode strings are a type of string that can handle characters from most of the world's writing systems. In Python 2.x, Unicode strings are indicated with the 'u' prefix, whereas in Python 3.x, all strings are Unicode strings by default.

How to get rid of the 'u' prefix

If we want to get rid of the 'u' prefix in a parsed JSON dictionary, we can use the str() method to convert the dictionary to a string and then convert the string back to a dictionary. This will remove the 'u' prefix from the keys and values. Here is an example:

```
import json

json_string = '{"name": "John", "age": 30, "city": "New York"}'
parsed_json = json.loads(json_string)
parsed_json_str = str(parsed_json)
parsed_json = json.loads(parsed_json_str)

print(parsed_json)
```

Output:
```
{'name': 'John', 'age': 30, 'city': 'New York'}
```

This method works by converting the dictionary to a string using str(), which removes the 'u' prefix. Then, the string is parsed back into a dictionary using json.loads(), resulting in a dictionary without the 'u' prefix.
