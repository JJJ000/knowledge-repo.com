---
title: Is it possible to transform a dictionary into a series of tuples?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-16 00:00:00
updated_at: 2023-04-16 00:00:00
tldr: Use the .items() method to convert the dictionary into a list of key-value tuples.
---

**Contents**

[TOC]

# Section 1: Introduction

In Python, a dictionary is a collection of key-value pairs. A list of tuples, on the other hand, is a collection of tuples where each tuple contains some elements. In some situations, we may need to convert a dictionary into a list of tuples. In this guide, we will explore different ways to achieve this goal.

# Section 2: Using dict.items() method

One way to convert a dictionary into a list of tuples is to use the dict.items() method. The dict.items() method returns a view object that contains tuples of (key, value) pairs in the dictionary. We can convert this view object into a list to get a list of tuples.

Here's an example:

```python
my_dict = {'a': 1, 'b': 2, 'c': 3}
my_list = list(my_dict.items())
print(my_list)
```

Output:
```
[('a', 1), ('b', 2), ('c', 3)]
```

In this example, we first define a dictionary `my_dict` that contains three key-value pairs. We then use the `dict.items()` method to get a view object that contains tuples of (key, value) pairs in `my_dict`. Finally, we convert this view object into a list using the `list()` function and store it in the variable `my_list`.

# Section 3: Using list comprehension

Another way to convert a dictionary into a list of tuples is to use a list comprehension. A list comprehension is a compact way to create a new list by transforming an existing list or other iterable.

Here's an example:

```python
my_dict = {'a': 1, 'b': 2, 'c': 3}
my_list = [(key, value) for key, value in my_dict.items()]
print(my_list)
```

Output:
```
[('a', 1), ('b', 2), ('c', 3)]
```

In this example, we use a list comprehension to iterate over the key-value pairs in `my_dict`. For each key-value pair, we create a new tuple that contains the key and value. We then use the `list()` function to convert the list comprehension into a list and store it in the variable `my_list`.

# Section 4: Conclusion

In this guide, we explored two different ways to convert a dictionary into a list of tuples in Python. The first method involves using the `dict.items()` method to get a view object that contains tuples of (key, value) pairs in the dictionary, and then converting this view object into a list. The second method involves using a list comprehension to iterate over the key-value pairs in the dictionary, and then creating a new tuple for each key-value pair. Both methods are simple and easy to understand, and you can choose the one that suits your needs.
