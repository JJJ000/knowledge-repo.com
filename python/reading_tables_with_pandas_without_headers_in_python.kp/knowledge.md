---
title: Pandas read a table without any column labels
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: Pandas can read in a table without headers using the `header=None` argument when using the `pd.read\_csv()` method.
---

**Contents**

[TOC]

# Section 1: Set Column Names

Pandas can read in a table without headers by specifying the column names manually. To do this, use the `names` argument in the `pd.read_csv()` function. For example, if the table has three columns, the following code can be used to set the column names:

```
pd.read_csv('filename.csv', names=['column1', 'column2', 'column3'])
```

# Section 2: Specify Header

If the table does not have a header row, pandas can be instructed to use the first row as the column names. To do this, use the `header` argument in the `pd.read_csv()` function. For example, the following code can be used to read in a table without a header row:

```
pd.read_csv('filename.csv', header=None)
```

# Section 3: Skip Rows

Pandas can also be instructed to skip a certain number of rows before reading the data. To do this, use the `skiprows` argument in the `pd.read_csv()` function. For example, the following code can be used to skip the first row of a table:

```
pd.read_csv('filename.csv', skiprows=1)
```

# Section 4: Set Index

Pandas can also be instructed to use a certain column as the index for the dataframe. To do this, use the `index_col` argument in the `pd.read_csv()` function. For example, the following code can be used to use the first column as the index for the dataframe:

```
pd.read_csv('filename.csv', index_col=0)
```
