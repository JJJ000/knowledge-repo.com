---
title: Reworded obtaining distinct values across several columns in pandas
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-08 00:00:00
updated_at: 2023-03-08 00:00:00
tldr: To get unique values for multiple columns in Pandas, use the `unique()` method on a DataFrame with the column names specified as a list.
---

**Contents**

[TOC]

Section 1: Introduction
-----------------------
Pandas is an open-source data manipulation and analysis library for Python. It provides a rich and powerful toolkit for working with structured data, and supports a wide range of data formats and sources, including CSV, Excel, SQL databases, and even web APIs. In this tutorial, we will explore how to find unique values across multiple columns in Pandas.

Section 2: Pandas Unique Function
-------------------------------
The Pandas `unique` function is used to find unique values in a Pandas series or dataframe column. It can also be used with multiple columns to find unique combinations of values across those columns. The syntax for using the `unique` function with Pandas dataframes is as follows:

```python
df[["column1", "column2"]].drop_duplicates()
```

Here, `df` is the Pandas dataframe, and `column1` and `column2` are the names of the columns to be considered. The `drop_duplicates` function removes any duplicate rows from the resulting dataframe.

Section 3: Example
-----------------
Let's consider an example to understand how to find unique values across multiple columns in Pandas. We have a Pandas dataframe with three columns - `Name`, `Country`, and `Age`:

```python
import pandas as pd

data = {
    "Name": ["John", "Mary", "Peter", "John"],
    "Country": ["USA", "Canada", "USA", "USA"],
    "Age": [25, 30, 35, 25]
}

df = pd.DataFrame(data)

print(df)
```

Output:
```
    Name Country  Age
0   John     USA   25
1   Mary  Canada   30
2  Peter     USA   35
3   John     USA   25
```

We want to find unique combinations of `Name` and `Country`. To do that, we can use the `unique` function as follows:

```python
unique_values = df[["Name", "Country"]].drop_duplicates()

print(unique_values)
```

Output:
```
    Name Country
0   John     USA
1   Mary  Canada
2  Peter     USA
```

Section 4: Conclusion
-----------------------
In this tutorial, we explored how to find unique values across multiple columns in Pandas. We used the `unique` function with the `drop_duplicates` function to achieve this. This is a useful technique for data preprocessing and cleaning, as well as for exploratory data analysis.
