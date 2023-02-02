---
title: Retrieve the initial entry in a specified column
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-01 00:00:00
updated_at: 2023-02-01 00:00:00
tldr: To get the first row value of a given column in Python, use the iloc[0] indexer.
---

**Contents**

[TOC]

##### Using Pandas

Pandas is a popular Python library for data analysis. It provides various methods for accessing data from a given column.

To get the first row value of a given column, you can use the `iloc` method. This method takes an integer position for each row and column. The syntax for this method is:

`df.iloc[0, column_index]`

Where `df` is the dataframe and `column_index` is the index of the column you want to access.

For example, if you have a dataframe named `df` and you want to access the first row value of the column at index 3, you can use the following code:

`df.iloc[0, 3]`
