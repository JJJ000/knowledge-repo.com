---
title: What is the process for adding new keys to a dictionary?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-01-08 00:00:00
updated_at: 2023-01-08 00:00:00
tldr: You can add new keys to a dictionary in Python by using the dictionary's `update()` method or by assigning a value to a new key.
---

**Contents**

[TOC]

### Creating a New Key-Value Pair

1. Create a variable that stores the dictionary.

```python
my_dict = {'key1': 'value1', 'key2': 'value2'}
```

2. Use the dictionary's `update()` method to add the new key-value pair.

```python
my_dict.update({'key3': 'value3'})
```

### Accessing the New Key-Value Pair

1. Use the dictionary's `get()` method to access the value associated with the new key.

```python
value3 = my_dict.get('key3')
```

2. Use the dictionary's `[]` notation to access the value associated with the new key.

```python
value3 = my_dict['key3']
```
