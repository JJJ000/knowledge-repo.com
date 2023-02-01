---
title: What is the syntax for retrieving the ith column from a numpy multidimensional array?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-01 00:00:00
updated_at: 2023-02-01 00:00:00
tldr: To access the ith column of a NumPy multidimensional array in Python, use array\_name[,i].
---

**Contents**

[TOC]

**Accessing a Single Column**

1. Get the desired column from the array using the slice notation. The syntax is `arr[:, i]`, where `arr` is the array and `i` is the index of the desired column.

**Accessing Multiple Columns**

1. Get the desired columns from the array using the slice notation. The syntax is `arr[:, i:j]`, where `arr` is the array, `i` is the index of the starting column and `j` is the index of the ending column.

**Accessing a Column by Name**

1. Get the desired column from the array using the column name. The syntax is `arr[column_name]`, where `arr` is the array and `column_name` is the name of the desired column.

**Accessing Multiple Columns by Name**

1. Get the desired columns from the array using the column names. The syntax is `arr[[column_name1, column_name2, ...]]`, where `arr` is the array and `column_name1`, `column_name2`, etc. are the names of the desired columns.
