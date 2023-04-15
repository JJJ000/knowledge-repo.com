---
title: What are the steps to generate a key or add an item to an existing key?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-16 00:00:00
updated_at: 2023-04-16 00:00:00
tldr: In Python, you can create a key or append an element to a key in a dictionary using square bracket notation.
---

**Contents**

[TOC]

# Creating a key in Python

In Python, a key is part of a collection called a dictionary. A dictionary is a collection of key-value pairs, where each key must be unique.

Here's how you can create a key in Python:

```
my_dict = {}  # create an empty dictionary
my_dict['key'] = 'value'  # add a key-value pair
```

In this example, we create an empty dictionary called `my_dict`. We then add a key-value pair using square brackets notation, where `'key'` is the key and `'value'` is the value.

You can also create a dictionary with multiple key-value pairs at once:

```
my_dict = {'key1': 'value1', 'key2': 'value2', 'key3': 'value3'}
```

In this example, we create a dictionary called `my_dict` with three key-value pairs.

# Appending an element to a key in Python

In Python, a key in a dictionary can have a value that is a list. You can append elements to this list using the `.append()` method.

Here's how you can append an element to a key in Python:

```
my_dict = {'key': ['value1', 'value2']}
my_dict['key'].append('value3')
```

In this example, we create a dictionary with a key called `'key'` whose value is a list with two elements. We then append a third element to this list using the `.append()` method.

You can also use the `.extend()` method to append multiple elements to a key's list:

```
my_dict = {'key': ['value1', 'value2']}
my_dict['key'].extend(['value3', 'value4'])
```

In this example, we create a dictionary with a key called `'key'` whose value is a list with two elements. We then use the `.extend()` method to append two more elements to this list.
