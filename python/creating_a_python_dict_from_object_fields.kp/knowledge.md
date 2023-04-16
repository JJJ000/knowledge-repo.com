---
title: Creating a Python dictionary from an object's attributes
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: You can create a Python dictionary from an object`s fields by looping through the object`s attributes and assigning each attribute to a key-value pair in the dictionary.
---

**Contents**

[TOC]

## Create Dictionary

We can create a Python dictionary from an object's fields using the `dict` function. The `dict` function takes a list of tuples, where each tuple contains a key and a value. The keys of the dictionary will be the first elements of the tuples, and the values will be the second elements.

For example, if we have an object `obj` with fields `name`, `age`, and `height`, we can create a dictionary from its fields like this:

```python
fields = [('name', obj.name), ('age', obj.age), ('height', obj.height)]
obj_dict = dict(fields)
```

## Access Dictionary Items

Once we have created the dictionary, we can access the items in the dictionary by using their keys. For example, if we want to access the value for the `name` key, we can do the following:

```python
name = obj_dict['name']
```

## Update Dictionary Items

We can also update the items in the dictionary by using their keys. For example, if we want to update the value for the `name` key, we can do the following:

```python
obj_dict['name'] = 'John'
```

## Delete Dictionary Items

Finally, we can also delete items from the dictionary by using their keys. For example, if we want to delete the `name` key from the dictionary, we can do the following:

```python
del obj_dict['name']
```
