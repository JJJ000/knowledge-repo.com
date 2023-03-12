---
title: The error message "typeerror 'dict_keys' object does not support indexing" can be restated as "attempting to index a dictionary keys object results in a type error."
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-12 00:00:00
updated_at: 2023-03-12 00:00:00
tldr: Dict keys cannot be accessed by indexing directly and need to be converted to a list or tuple before they can be indexed.
---

**Contents**

[TOC]

Section 1: Explanation of the error
The error "TypeError: 'dict_keys' object does not support indexing" occurs when we try to access a specific element from a dictionary using an index with the keys() method. This error happens because the keys() method doesn't return a list of keys, but instead, it returns a view object which is a dynamic view of the dictionary keys. 

Section 2: How to reproduce the error
To reproduce the error, we can create a dictionary and try to access a specific element using an index with the keys() method. For example:

```
my_dict = {'key1': 'value1', 'key2': 'value2', 'key3': 'value3'}
print(my_dict.keys()[0])
```

This code will result in the following error: "TypeError: 'dict_keys' object does not support indexing".

Section 3: How to fix the error
To fix the error, we can convert the dict_keys object into a list using the list() method. For example:

```
my_dict = {'key1': 'value1', 'key2': 'value2', 'key3': 'value3'}
keys_list = list(my_dict.keys())
print(keys_list[0])
```

This code will print the first element of the keys_list which is 'key1' in this case.

Section 4: Conclusion
The 'dict_keys' object doesn't support indexing because it's a view object and not a list. To fix this error, we can convert the dict_keys object to a list using the list() method or use a loop to iterate through the keys.
