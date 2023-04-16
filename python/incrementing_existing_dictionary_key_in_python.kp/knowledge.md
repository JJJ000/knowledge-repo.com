---
title: Verify if a specified key is already present in the dictionary and increase its value
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: If the key exists in the dictionary, use the dictionary`s update() method to increment its value.
---

**Contents**

[TOC]

### Section 1: Check if Key Exists

We can use the `in` keyword to check if a given key exists in a dictionary:

```python
my_dict = {'key1': 'value1', 'key2': 'value2'}

if 'key1' in my_dict:
    print('Key exists!')
```

### Section 2: Increment Value

Once we have confirmed that the key exists, we can increment its value by one using the `+=` operator:

```python
my_dict = {'key1': 1, 'key2': 2}

if 'key1' in my_dict:
    my_dict['key1'] += 1
```

### Section 3: Conditional Increment

We can also add a conditional statement to check if the value of the key is greater than or equal to a certain number before incrementing it:

```python
my_dict = {'key1': 1, 'key2': 2}

if 'key1' in my_dict and my_dict['key1'] >= 5:
    my_dict['key1'] += 1
```

### Section 4: Increment by Amount

Finally, we can also increment the value of the key by a certain amount:

```python
my_dict = {'key1': 1, 'key2': 2}

if 'key1' in my_dict:
    my_dict['key1'] += 10
```
