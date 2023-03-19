---
title: How can one obtain the nth element of a Python list, or a default value if the element is not present?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-08 00:00:00
updated_at: 2023-03-08 00:00:00
tldr: Use list indexing with the desired index followed by a default value provided by the `get()` method of the list, like this `my\_list[n] if n < len(my\_list) else default\_value`.
---

**Contents**

[TOC]

Getting the nth Element of a Python List

To get the nth element of a Python list, you can use the indexing operator (`[]`) with the index `n-1`. For example, to get the third element of a list `my_list`, you would use:

```python
my_list[2]
```

This is because Python uses zero-based indexing, which means that the first element of a list has an index of 0, the second element has an index of 1, and so on.

Handling Index Errors

If the index `n-1` is out of range for the list, Python will raise an `IndexError`. To handle this error, you can use a `try`/`except` block. For example, to get the third element of a list `my_list`, or return `None` if the list is too short, you would use:

```python
try:
    element = my_list[2]
except IndexError:
    element = None
```

Using a Default Value

If you want to get a default value instead of `None` when the index is out of range, you can use the `get()` method of the list object. The `get()` method takes two arguments: the index that you want to get, and a default value to return if the index is out of range. For example, to get the third element of a list `my_list`, or return `0` if the list is too short, you would use:

```python
element = my_list.get(2, 0)
```

In this example, `2` is the index that we want to get, and `0` is the default value to return if the index is out of range.
