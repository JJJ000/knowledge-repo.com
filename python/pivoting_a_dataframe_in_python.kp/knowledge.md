---
title: What is the best way to rearrange a dataframe?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-01 00:00:00
updated_at: 2023-02-01 00:00:00
tldr: You can pivot a dataframe in Python using the pandas.DataFrame.pivot() method.
---

**Contents**

[TOC]

### Using the Pandas Pivot Function
The Pandas library provides a convenient `pivot()` function that can be used to pivot a dataframe. This function takes three arguments: `index`, `columns`, and `values`. The `index` argument specifies the column that should be used as the row labels of the resulting dataframe. The `columns` argument specifies the column that should be used as the column labels of the resulting dataframe. Finally, the `values` argument specifies the column to be used for populating the values in the resulting dataframe.

### Example 
For example, consider the following dataframe:

| ID | Name | Age |
|----|------|-----|
| 1  | John | 20  |
| 2  | Jane | 22  |
| 3  | Joe  | 21  |

We can use the `pivot()` function to pivot this dataframe and create a new dataframe with the Age column as the values:

```
pivot_df = df.pivot(index='ID', columns='Name', values='Age')
```

This will result in the following dataframe:

|    | John | Jane | Joe  |
|----|------|------|------|
| ID |  20  |  22  |  21  |

### Using the Pandas Melt Function
Alternatively, the Pandas library also provides a `melt()` function that can be used to pivot a dataframe. This function takes several arguments, including `id_vars`, `value_vars`, and `var_name`. The `id_vars` argument specifies the columns to be used as the identifier variables. The `value_vars` argument specifies the columns to be used as the value variables. Finally, the `var_name` argument specifies the name of the variable column in the resulting dataframe.

### Example
For example, consider the same dataframe as in the previous example:

| ID | Name | Age |
|----|------|-----|
| 1  | John | 20  |
| 2  | Jane | 22  |
| 3  | Joe  | 21  |

We can use the `melt()` function to pivot this dataframe and create a new dataframe with the Age column as the values:

```
pivot_df = df.melt(id_vars='ID', value_vars='Age', var_name='Name')
```

This will result in the following dataframe:

| ID | Name | Age |
|----|------|-----|
| 1  | John | 20  |
| 2  | Jane | 22  |
| 3  | Joe  | 21  |
