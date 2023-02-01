---
title: Retrieve a random item from a dictionary in python
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-01 00:00:00
updated_at: 2023-02-01 00:00:00
tldr: To access an arbitrary element in a dictionary, use the dictionary`s key to index into the dictionary.
---

**Contents**

[TOC]

# Accessing an Element

To access an element in a dictionary in Python, we use the syntax `dictionary[key]`. This will return the value associated with the given key in the dictionary.

# Example

Let's say we have the following dictionary:

```
my_dict = {
    "name": "John",
    "age": 20,
    "city": "New York"
}
```

To access the value associated with the key `"name"`, we can use the syntax `my_dict["name"]`. This will return the value `"John"`.

# Output

The output of the code `my_dict["name"]` would be `John`.
