---
title: How to access an element in dict_keys using an index in python3?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-18 00:00:00
updated_at: 2023-04-18 00:00:00
tldr: It is not possible to access dict\_keys element by index in Python3 because dict\_keys object does not support indexing.
---

**Contents**

[TOC]

Section 1: Introduction
In Python, dictionary is a built-in data type. When we create a dictionary, we get two types of objects, i.e., keys and values. Just like a list, we can access the dictionary elements by index, but only in limited scenarios. In this article, we will explore how to access dict_keys element by index in Python3.

Section 2: The dict_keys object
Before delving deeper into the topic, we must first understand the dict_keys object. A dict_keys object is a view object that contains the keys of a dictionary. The dict_keys object provides us with a dynamic view of the dictionary keys. Moreover, the dict_keys object can be sliced like a list, but we cannot access it by index directly.

Section 3: Dictionary index access using dict_keys object
To access the dictionary element by index, we first get a list of keys using the keys() method of the dictionary. Then, we can access each element by its index value. The following code example demonstrates this approach.

```python
my_dict = {'name': 'John', 'age': 30, 'city': 'New York'}
keys_list = list(my_dict.keys())
print(keys_list[0])  # Output: 'name'
```

Section 4: Conclusion
In conclusion, we can access the dict_keys element by index indirectly by first converting the dict_keys object to a list and then accessing the list elements by index. However, it is to be noted that if the dictionary is manipulated after converting the dict_keys object to a list, then the index value might not match the required key. Therefore, it is always recommended to iterate over the dictionary keys instead of accessing it by index.
