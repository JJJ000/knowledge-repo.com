---
title: Retrieving dict keys as if they were an attribute?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: It is not possible to access dict keys like an attribute in Python.
---

**Contents**

[TOC]

#### Accessing Dictionary Keys

Dictionaries are a powerful data type in Python that allow us to store and access key-value pairs. We can access the values in a dictionary using the keys associated with them. This can be done in two ways:

##### Using Square Brackets

The most common way to access dictionary keys is to use square brackets and the key name. This will return the value associated with that key. For example, if we have a dictionary called "my_dict" with a key "name" and a value "John", we can access the value by doing:

```
value = my_dict["name"]
```

##### Using Get Method

We can also use the get() method to access dictionary keys. This is useful if we want to provide a default value if the key does not exist. For example, if we have a dictionary called "my_dict" with a key "name" and a value "John", we can access the value by doing:

```
value = my_dict.get("name", "default_value")
```

This will return the value associated with the key "name" if it exists, or "default_value" if it does not.
