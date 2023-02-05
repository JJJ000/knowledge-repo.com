---
title: What is the distinction between the filter and filter_by functions in sqlalchemy?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: The filter() method applies a given filter criterion to the query, whereas the filter\_by() method applies a given filter criterion to the query based on keyword arguments.
---

**Contents**

[TOC]

# FILTER
Filter is used to filter a query based on given criteria. It takes in an expression that can be a column, an operator, and a value. The expression is then evaluated to determine whether a given record matches the criteria.

# FILTER_BY
Filter_by is similar to filter, but instead of taking an expression, it takes a dictionary of column names and values. This dictionary is then used to filter the query. The advantage of this method is that it allows for multiple criteria to be specified at once, making the query more efficient.
