---
title: What are the guidelines followed by pandas in order to produce a view or a copy?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Pandas uses the `copy-on-write` concept to generate a view vs a copy in Python.
---

**Contents**

[TOC]

# Background
Before diving into the rules that Pandas uses to generate a view versus a copy in Python, it is important to understand what a view and a copy mean when it comes to data in Pandas.

A view is a reference to the same underlying data as the original object. When we make changes to the view, the changes are also reflected in the original object. In other words, a view points to the same data in memory as the original object.

A copy, on the other hand, is an entirely new object with its own data. When we make changes to a copy, the original object remains unchanged. In other words, a copy points to a different location in memory than the original object.

# Rules for Generating a View
Pandas generates a view under the following conditions:
1. When using slicing to extract rows from a DataFrame
2. When using the `.loc` and `.iloc` methods to extract rows and/or columns from a DataFrame
3. When using the `.head()` method to extract the top n rows of a DataFrame
4. When using the `.tail()` method to extract the bottom n rows of a DataFrame

It is important to note that these rules apply only when the DataFrame being sliced or extracted is not itself a subset of another DataFrame.

# Rules for Generating a Copy
Pandas generates a copy under the following conditions:
1. When using conditional indexing to extract rows from a DataFrame
2. When using boolean indexing to extract rows from a DataFrame
3. When using the `.copy()` method to create a copy of a DataFrame

It is important to note that these rules apply when the subset of the DataFrame being extracted is not continuous, i.e., it is a non-contiguous subset of rows and/or columns.

# Conclusion
In conclusion, Pandas uses specific rules to determine whether a view or a copy should be generated when extracting data from a DataFrame. Understanding these rules is important to ensure that we are working with the data we expect, whether it is a view or a copy.
