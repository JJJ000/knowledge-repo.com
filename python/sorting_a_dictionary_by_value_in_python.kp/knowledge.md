---
title: What is the process for ordering a dictionary by value?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-01-08 00:00:00
updated_at: 2023-01-08 00:00:00
tldr: You can sort a dictionary by value in Python using the `sorted()` function with the key parameter set to the dictionary's values.
---

**Contents**

[TOC]

### Overview

Sorting a dictionary by value in Python is a common task that can be accomplished using a variety of methods. The two most popular methods are using the built-in `sorted()` function or using the `operator.itemgetter()` method. 

### Using the sorted() Function

The `sorted()` function can be used to sort a dictionary by value in Python. This can be done by passing the dictionary to the sorted() function along with a `key` argument that specifies the value of the dictionary to be used for sorting. For example, to sort a dictionary by its values in ascending order:

```python
sorted_dict = sorted(dictionary, key=dictionary.get)
```

### Using the operator.itemgetter() Method

The `operator.itemgetter()` method can also be used to sort a dictionary by value in Python. This can be done by passing the `operator.itemgetter()` method to the sorted() function along with the dictionary. For example, to sort a dictionary by its values in descending order:

```python
sorted_dict = sorted(dictionary.items(), key=operator.itemgetter(1), reverse=True)
```

### Conclusion

Sorting a dictionary by value in Python can be accomplished using either the built-in sorted() function or the operator.itemgetter() method. Both methods are fairly easy to use and can be used to sort a dictionary by its values in either ascending or descending order.
