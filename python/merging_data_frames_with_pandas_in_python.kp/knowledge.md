---
title: Combine two data frames in pandas using multiple columns as the joining keys
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: Pandas can merge two data frames on multiple columns using the merge() function with the specified columns as the keys argument.
---

**Contents**

[TOC]

#### Solution 1: Using Pandas Merge

Pandas merge() is a function used to join two data frames on one or more columns. It is a powerful tool for combining datasets, and can be used to join data frames on multiple columns.

To use Pandas merge, the two data frames must have the same column names. The syntax for merging two data frames is as follows:

`pd.merge(df1, df2, on=['column_name1', 'column_name2'])`

The above syntax will join the two data frames on the specified columns.

#### Solution 2: Using Pandas Join

Pandas join() is another function used to join two data frames on one or more columns. It is similar to merge, but is more flexible in terms of the data types of the columns used for joining.

To use Pandas join, the two data frames must have the same column names. The syntax for joining two data frames is as follows:

`pd.join(df1, df2, on=['column_name1', 'column_name2'])`

The above syntax will join the two data frames on the specified columns.

#### Solution 3: Using SQL

SQL can also be used to join two data frames on multiple columns. The syntax for joining two data frames is as follows:

`SELECT * FROM df1 INNER JOIN df2 ON df1.column_name1 = df2.column_name1 AND df1.column_name2 = df2.column_name2`

The above syntax will join the two data frames on the specified columns.

#### Solution 4: Using Pandas Concat

Pandas concat() is another function used to join two data frames on one or more columns. It is a powerful tool for combining datasets, and can be used to join data frames on multiple columns.

To use Pandas concat, the two data frames must have the same column names. The syntax for concatenating two data frames is as follows:

`pd.concat([df1, df2], axis=1, join='inner')`

The above syntax will join the two data frames on the specified columns.
