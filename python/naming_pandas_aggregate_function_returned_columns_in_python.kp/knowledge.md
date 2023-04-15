---
title: How can you assign new column names when using the pandas aggregate function?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-18 00:00:00
updated_at: 2023-04-18 00:00:00
tldr: To name returned columns in Pandas aggregate function, use dictionary comprehension with column names as keys and aggregation functions as values inside the `agg()` method.
---

**Contents**

[TOC]

Section 1: Introduction
Pandas is one of the most widely-used libraries for data manipulation in Python. Being widely-used means that there are many different methods for solving the same problems. One such problem is how to name the returned columns in a Pandas aggregate function.

Section 2: The Problem
Suppose we have a DataFrame with columns 'A', 'B', and 'C'. We want to group by column 'A' and calculate the mean of column 'B'. We use the Pandas aggregate function to do this:

```
grouped_df = df.groupby('A').agg({'B': 'mean'})
```

The resulting DataFrame has one column, named 'B', instead of the desired name, 'B_mean'.

Section 3: Solution
To name the returned columns in a Pandas aggregate function, we can use the Pandas MultiIndex.

```
grouped_df = df.groupby('A').agg(B_mean=('B', 'mean'))
```

Here, we are using the MultiIndex to specify the name of the returned column. The first element in the tuple ('B_mean') is the desired name of the returned column, and the second element ('B', 'mean') specifies the column to be used for aggregation ('B') and the method to use for aggregation ('mean').

Section 4: Conclusion
In summary, we can name the returned columns in a Pandas aggregate function using the MultiIndex. By specifying the name of the returned column in the MultiIndex, we can achieve more descriptive column names, making our resulting DataFrame more clear and easier to understand.
