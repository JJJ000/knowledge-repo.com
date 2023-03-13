---
title: What distinguishes the use of loc from the use of square brackets when filtering for columns in pandas/python?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-13 00:00:00
updated_at: 2023-03-13 00:00:00
tldr: Using loc allows for both label-based indexing and filtering based on conditions, while using square brackets only allows for column selection by label or a list of labels.
---

**Contents**

[TOC]

Introduction

Filtering for columns in Pandas/Python is a common task when working with dataframes, and there are two different methods for doing so: using loc and using just square brackets. While both methods can produce the same results, there are some key differences between the two that can affect how you use them in your code.

Section 1: Syntax

The first difference between using loc and using square brackets to filter for columns is their syntax. When using square brackets, you simply pass a list of column names to the dataframe. For example, if you had a dataframe with columns 'A', 'B', and 'C', you could filter for just columns 'A' and 'B' like this:

```
df[['A', 'B']]
```

On the other hand, when using loc, you need to specify both rows and columns. If you want to filter for all rows and just columns 'A' and 'B', you would need to use this syntax:

```
df.loc[:, ['A', 'B']]
```

Section 2: Indexing

Another key difference between loc and square brackets is how they index the columns of a dataframe. When you use square brackets, you can only access columns by their names. For example, if you had a dataframe with a column named 'A', you could access it like this:

```
df['A']
```

However, if you wanted to access column 'A' using loc, you would need to use the syntax:

```
df.loc[:, 'A']
```

In other words, when using loc, you need to specify both rows and columns, even if you just want to access a single column.

Section 3: Conditional filtering

One advantage of using loc over square brackets is that it allows for more complex conditional filtering. For example, if you wanted to filter for rows where column A is greater than 5 and column B is less than 10, you could use the syntax:

```
df.loc[(df['A'] > 5) & (df['B'] < 10)]
```

This is not possible with square brackets alone, as they only allow you to access specific columns by name.

Section 4: Performance

Finally, it's worth noting that there can be a difference in performance between using loc and using square brackets. In general, using square brackets is faster, as it involves less overhead. If you're working with a very large dataframe and speed is a concern, you may want to consider using square brackets instead of loc, unless you need the additional features and flexibility that loc provides.

Conclusion

In summary, there are several differences between using loc and using square brackets to filter for columns in Pandas/Python. While both methods can produce the same results, loc allows for more complex conditional filtering and requires more specific syntax, while square brackets are faster and allow for simpler column access by name. It's important to understand these differences so you can choose the method that best fits your needs when working with dataframes.
