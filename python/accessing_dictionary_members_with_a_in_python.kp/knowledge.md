---
title: What is the syntax for accessing members of a dictionary using a dot?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-02 00:00:00
updated_at: 2023-02-02 00:00:00
tldr: A dot `.` can be used to access members of a dictionary by specifying the dictionary name followed by the key of the desired value.
---

**Contents**

[TOC]

# Syntax

The syntax for accessing members of a dictionary using the dot operator is as follows:

`dictionary_name.key`

# Example

For example, if we have a dictionary with the following key-value pairs:

```
my_dict = {
    "name": "John Doe",
    "age": 30
}
```

We can access the value of the "name" key using the dot operator:

`my_dict.name`

This will return the value "John Doe".

# Caveats

It is important to note that the dot operator will only work if the key is a valid Python identifier. This means that it must start with a letter or underscore, and can only contain letters, numbers, and underscores. If the key is not a valid Python identifier, you must use the bracket notation instead:

`my_dict["name"]`
