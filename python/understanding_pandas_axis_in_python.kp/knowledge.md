---
title: What is the meaning of the 'axis' term in the pandas library?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: In pandas, an axis refers to a single dimension of a data structure, such as rows or columns.
---

**Contents**

[TOC]

# Definition

Axis in pandas is the number of dimensions of the dataframe. It is used to determine the direction of operations in a dataframe.

# Types of Axis

There are two types of axis in pandas:
1. Row axis - 0
2. Column axis - 1

# Examples

To illustrate the concept of axis, let's consider a dataframe with two columns and three rows.

|   | A | B |
|---|---|---|
| 0 | 1 | 2 |
| 1 | 3 | 4 |
| 2 | 5 | 6 |

In this dataframe, the row axis is 0 and the column axis is 1.
