---
title: Could you explain the distinction between join and merge functions in pandas?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: The difference between join and merge in Pandas is that join is used to combine data based on the index column, while merge is used to combine data based on one or more common columns.
---

**Contents**

[TOC]

# Introduction

Pandas is a Python library that is used for data manipulation and analysis. Pandas provides two ways to combine data, which are `join` and `merge`. Both of them are used to combine two or more dataframes into a single dataframe. However, the key difference between `join` and `merge` are in the way they are used and the operation they perform.

# Join

A join operation is used to combine two or more dataframes using a column or an index as a reference. When two dataframes are joined, the resulting dataframe will have all the rows from both dataframes that match the join criteria.

## Types of joins

Pandas provides four types of join operations, which are the `inner join`, `outer join`, `left join`, and `right join`.

### Inner Join

An inner join returns only those rows that have matching values in both dataframes. In other words, it returns the intersection of two dataframes. To perform an inner join in Pandas, we can use the `merge` function.

### Outer Join

An outer join returns all the rows that are present in both dataframes, along with the non-matching rows from both dataframes. In other words, it returns the union of two dataframes. To perform an outer join in Pandas, we can use the `merge` function.

### Left Join

A left join returns all the rows from the left dataframe and the matching rows from the right dataframe. If there are no matching rows in the right dataframe, the resulting dataframe will contain NaN values. To perform a left join in Pandas, we can use the `merge` function.

### Right Join

A right join returns all the rows from the right dataframe and the matching rows from the left dataframe. If there are no matching rows in the left dataframe, the resulting dataframe will contain NaN values. To perform a right join in Pandas, we can use the `merge` function.


# Merge

A merge operation is used to combine two or more dataframes into a single dataframe based on the values of the columns in the dataframes. Unlike a join operation, a merge operation does not require a reference column or index. Instead, it looks for matching rows in the dataframes based on the values in one or more columns. When two dataframes are merged, the resulting dataframe will have all the rows from both dataframes that match the merge criteria.

## Types of merges

Pandas provides three types of merge operations, which are the `inner merge`, `outer merge`, and `cross merge`.

### Inner Merge

An inner merge returns only those rows that have matching values in both dataframes based on a common column. In other words, it returns the intersection of two dataframes. To perform an inner merge in Pandas, we can use the `merge` function.

### Outer Merge

An outer merge returns all the rows that are present in both dataframes, along with the non-matching rows from both dataframes based on a common column. In other words, it returns the union of two dataframes. To perform an outer merge in Pandas, we can use the `merge` function.

### Cross Merge

A cross merge returns all possible combinations of rows from both dataframes. In other words, it returns the Cartesian product of two dataframes. To perform a cross merge in Pandas, we can use the `merge` function with the `how='cross'` parameter. This type of merge is not commonly used because it can result in a very large dataframe.
