---
title: Specifying the type of a collection using type hinting
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-05 00:00:00
updated_at: 2023-03-05 00:00:00
tldr: To type hint a collection of a specified type in Python, use the syntax List[Type].
---

**Contents**

[TOC]

Introduction
---

Python is a dynamically-typed language, meaning the type of the object is inferred at runtime rather than compile time. This can lead to unexpected errors when working with collections of mixed data types. Type hinting provides a way to annotate code with the types that variables and functions should be. This allows for better readability, static analysis, and can help prevent bugs.

Type Hinting Collections
---

Using type hinting, we can specify the types of elements in a collection, such as a list or a dictionary. This helps to ensure that all items in the collection are of the correct type and can prevent type-related errors at runtime. Here are some examples of how to type hint a collection of a specified type in Python:

1. Type hinting a list of specified type:

```python
from typing import List

def square_nums(nums: List[int]) -> List[int]:
    return [num ** 2 for num in nums]
```

In the above example, we have used the `List` type hint to specify that the `nums` parameter is a list of integers. The `-> List[int]` indicates that the function will return a list of integers.

2. Type hinting a dictionary with specified key-value types:

```python
from typing import Dict

def sort_dict_by_values(d: Dict[str, int]) -> Dict[str, int]:
    return {k: v for k, v in sorted(d.items(), key=lambda item: item[1])}
```

This function takes a dictionary where the keys are strings and the values are integers. The `Dict` type hint has been used to specify the types of both the keys and values in the dictionary.

3. Type hinting a set of specified type:

```python
from typing import Set

def remove_duplicates(nums: Set[int]) -> Set[int]:
    return set(nums)
```

This function takes a set of integers and returns a set of distinct integers. The `Set` type hint has been used to specify that the `nums` parameter is a set of integers.

Conclusion
---

Type hinting collections in Python can help to prevent type-related errors as well as improve code readability and maintainability. The `List`, `Dict`, and `Set` types can be used to specify the types of elements in a collection. When using type hinting, it is important to ensure that the types are accurate and consistent throughout the codebase.
