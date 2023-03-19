---
title: Adding to a list within a Python dictionary
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-16 00:00:00
updated_at: 2023-03-16 00:00:00
tldr: To append to a list in a Python dictionary, use the dictionary key to access the list and then use the append method to add the desired value to the end of the list.
---

**Contents**

[TOC]

1. Initializing a dictionary with an empty list
To append to a list in a Python dictionary, you must first create a dictionary and initialize the list with an empty one. This can be done using the curly braces notation or the built-in `dict()` function.

```python
my_dict = {}
my_dict['my_list'] = []

# or 

my_dict = dict()
my_dict['my_list'] = []
```

2. Using the append method to add items to the list
Once the list has been initialized, you can use the `append()` method to add items to the list. You simply reference the list in the dictionary using its key and call the `append()` method on it.

```python
my_dict['my_list'].append('item 1')
my_dict['my_list'].append('item 2')
my_dict['my_list'].append('item 3')
```

3. Appending multiple items to a list using the extend method
If you need to add multiple items to the dictionary list at once, you can use the `extend()` method. This method takes an iterable argument and adds each item from the iterable to the end of the list.

```python
my_dict['my_list'].extend(['item 4', 'item 5', 'item 6'])
```

4. Using the setdefault method to avoid KeyError
If the list does not already exist in the dictionary, calling `my_dict['my_list'].append()` will raise a KeyError exception. One way to avoid this is to use the `setdefault()` method, which allows you to set a default value for a key if it does not yet exist. The default value, in this case, would be an empty list.

```python
my_dict.setdefault('my_list', [])
my_dict['my_list'].append('item 7')
```
