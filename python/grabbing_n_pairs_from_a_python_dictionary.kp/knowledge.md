---
title: Retrieve the initial n key-value pairs from the dictionary
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-08 00:00:00
updated_at: 2023-03-08 00:00:00
tldr: Use dictionary comprehension to generate a new dictionary with the desired number of keyvalue pairs using the `list()` and `iter()` functions to iterate over the original dictionary`s items.
---

**Contents**

[TOC]

Section 1: Introduction
Python dictionary is a collection of key-value pairs. It is an unordered data type that is used to store data in the form of key-value pairs. Python provides various methods to manipulate dictionaries, and one such method is to return the first N key-value pairs from the dictionary. In this tutorial, we will discuss how to return the first N key-value pairs from a dictionary in Python.

Section 2: Using the items() function
The items() function in Python is used to return a list of dictionary's (key, value) tuple pairs. Here, we can use slicing to get the first N key-value pairs. The syntax of this function is as follows:

```
dictionary.items()
```

To get the first N key-value pairs, we can slice the list returned by the items() function:
```
dictionary.items()[:N]
```

For example, consider the following dictionary:

```python
my_dict = {'a': 1, 'b': 2, 'c': 3, 'd': 4, 'e': 5}
```

To return the first 3 key-value pairs from this dictionary, we can use the following code:

```python
first_three_pairs = dict(my_dict.items()[:3])
print(first_three_pairs)
```

Output:
```
{'a': 1, 'b': 2, 'c': 3}
```

Section 3: Using the list function
Another way to return the first N key-value pairs from a dictionary is to convert the dictionary into a list of (key, value) tuples and then slice the list. The syntax for this method is as follows:

``` python
list(dictionary.items())
```

To get the first N key-value pairs, we can slice the list returned by the list() function:
``` python
list(dictionary.items())[:N]
```

For example, consider the same dictionary as in the previous example:

```python
my_dict = {'a': 1, 'b': 2, 'c': 3, 'd': 4, 'e': 5}
```

To return the first 3 key-value pairs from this dictionary, we can use the following code:

```python
first_three_pairs = dict(list(my_dict.items())[:3])
print(first_three_pairs)
```

Output:
```
{'a': 1, 'b': 2, 'c': 3}
```

Section 4: Using the islice() function
The islice() function in Python is used to slice a list or an iterable object. Here, we can use the islice() function to slice the list of (key, value) tuples returned by the items() function. The syntax for this method is as follows:

```python
from itertools import islice
islice(iterable, start, stop)
```

To get the first N key-value pairs, we can use the islice() function with a stop value of N. For example, consider the same dictionary as in the previous examples:

```python
my_dict = {'a': 1, 'b': 2, 'c': 3, 'd': 4, 'e': 5}
```

To return the first 3 key-value pairs from this dictionary, we can use the following code:

```python
first_three_pairs = dict(islice(my_dict.items(), 3))
print(first_three_pairs)
```

Output:
```
{'a': 1, 'b': 2, 'c': 3}
```
