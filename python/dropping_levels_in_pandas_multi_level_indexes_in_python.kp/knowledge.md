---
title: How can I remove a level from a multi-level column index in pandas?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: Pandas can drop a level from a multi-level column index by using the `droplevel` method.
---

**Contents**

[TOC]

**Section 1: Overview**

Pandas is a powerful Python library for data analysis. It provides a wide range of tools for manipulating data, including the ability to drop a level from a multi-level column index. This can be useful when dealing with complex data sets with multiple levels of hierarchy.

**Section 2: Dropping a Level from a Multi-level Column Index**

Dropping a level from a multi-level column index in Pandas is relatively straightforward. To do so, you must use the `.droplevel()` method. This method takes the name of the level you want to drop as an argument. 

For example, if you have a DataFrame with a multi-level column index like this:

```python
df = pd.DataFrame({
    'A': [1, 2, 3],
    'B': [4, 5, 6],
    'C': [7, 8, 9],
    'D': [10, 11, 12]
}, index=pd.MultiIndex.from_tuples([
    ('a', 'x'),
    ('a', 'y'),
    ('b', 'z')
], names=['first', 'second']))
```

You can drop the `second` level of the index like this:

```python
df.columns = df.columns.droplevel('second')
```

**Section 3: Results**

After dropping the `second` level of the index, the DataFrame will look like this:

```python
      A  B  C   D
first              
a      1  4  7  10
a      2  5  8  11
b      3  6  9  12
```

**Section 4: Conclusion**

In summary, dropping a level from a multi-level column index in Pandas is a straightforward process. It can be achieved using the `.droplevel()` method, which takes the name of the level you want to drop as an argument. After dropping the level, the DataFrame will no longer include the dropped level in its column index.
