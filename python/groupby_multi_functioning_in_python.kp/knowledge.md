---
title: Apply multiple functions to multiple columns when performing a groupby operation
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: You can use the agg() function to apply multiple functions to multiple groupby columns in Python.
---

**Contents**

[TOC]

### Solution 1: 
Using `apply()` Method:

The `apply()` method can be used to apply multiple functions to multiple groupby columns in Python. This can be done by passing a list of functions to the `apply()` method, and then passing the list of columns to the `groupby()` method. For example:

```python
df.groupby(['column1', 'column2']).apply(lambda x: [func1(x), func2(x), func3(x)])
```

### Solution 2: 
Using `agg()` Method:

The `agg()` method can also be used to apply multiple functions to multiple groupby columns in Python. This can be done by passing a dictionary of functions to the `agg()` method, and then passing the list of columns to the `groupby()` method. For example:

```python
df.groupby(['column1', 'column2']).agg({'column1': func1, 'column2': func2, 'column3': func3})
```

### Solution 3: 
Using `transform()` Method:

The `transform()` method can also be used to apply multiple functions to multiple groupby columns in Python. This can be done by passing a dictionary of functions to the `transform()` method, and then passing the list of columns to the `groupby()` method. For example:

```python
df.groupby(['column1', 'column2']).transform({'column1': func1, 'column2': func2, 'column3': func3})
```

### Solution 4: 
Using `apply()` and `agg()` Methods:

The `apply()` and `agg()` methods can also be used together to apply multiple functions to multiple groupby columns in Python. This can be done by passing a dictionary of functions to the `apply()` method and a list of functions to the `agg()` method, and then passing the list of columns to the `groupby()` method. For example:

```python
df.groupby(['column1', 'column2']).apply(lambda x: {'column1': func1(x), 'column2': func2(x), 'column3': func3(x)}).agg({'column1': func4, 'column2': func5, 'column3': func6})
```
