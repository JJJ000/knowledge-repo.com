---
title: Divide a single string entry in a pandas dataframe into multiple rows
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: Use the `str.split()` method to split the string into separate values and then assign each value to a new row.
---

**Contents**

[TOC]

### Section 1: Using str.split()

The `str.split()` method can be used to split a string into separate rows in a pandas dataframe. The syntax for this method is `dataframe[column_name].str.split(separator, expand=True)`.

The `separator` argument is used to specify the character or string that will be used to separate the string into separate rows. The `expand` argument is used to specify whether the string should be split into multiple columns or multiple rows. If `expand=True`, the string will be split into multiple rows.

### Section 2: Example

For example, if we have a dataframe with a column containing strings as follows:

| id | string | 
|----|--------| 
| 1  | ab,cd  | 
| 2  | ef,gh  |

We can use the `str.split()` method to split the strings into separate rows as follows:

```
df[‘string’].str.split(‘,’, expand=True)

```

This will result in the following dataframe:

| id | 0 | 1 | 
|----|---|---| 
| 1  | ab | cd | 
| 2  | ef | gh |

### Section 3: Multiple Separators

The `str.split()` method also supports multiple separators. For example, if we have a dataframe with a column containing strings as follows:

| id | string | 
|----|--------| 
| 1  | ab;cd  | 
| 2  | ef,gh  |

We can use the `str.split()` method to split the strings into separate rows using both the `;` and `,` characters as separators as follows:

```
df[‘string’].str.split(‘[;,]’, expand=True)

```

This will result in the following dataframe:

| id | 0 | 1 | 2 | 
|----|---|---|---| 
| 1  | ab |   | cd | 
| 2  | ef | gh |   |

### Section 4: Handling Missing Values

By default, the `str.split()` method will replace any missing values with `NaN` values. If we want to preserve the original values, we can use the `na_filter` argument to specify which values should be replaced with `NaN`. For example, if we want to replace only empty strings with `NaN` values, we can use the following syntax:

```
df[‘string’].str.split(‘[;,]’, expand=True, na_filter=False)

```
