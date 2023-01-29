---
title: What is the best way to create a dictionary (dict) using separate lists of keys and values?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: Use the dict() constructor to create a dictionary from separate lists of keys and values.
---

**Contents**

[TOC]

### Section 1: Create the Lists

The first step is to create the two lists - one for the keys and one for the values. The lists should have the same number of elements.

```python
keys = ["name", "age", "city"]
values = ["John", 25, "New York"]
```

### Section 2: Create the Dictionary

The next step is to create the dictionary. This can be done by using the `dict()` function and passing in the two lists.

```python
my_dict = dict(zip(keys, values))
```

### Section 3: Check the Dictionary

Finally, you can check the dictionary to make sure that the keys and values have been correctly assigned.

```python
print(my_dict)

# Output: {'name': 'John', 'age': 25, 'city': 'New York'}
```

### Section 4: Access the Dictionary

You can also access the dictionary elements by using the keys.

```python
name = my_dict["name"]
print(name)

# Output: John
```
