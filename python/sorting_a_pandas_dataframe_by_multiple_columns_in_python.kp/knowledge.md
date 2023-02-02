---
title: What is the process for sorting a pandas dataframe in Python by two or more columns?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-02 00:00:00
updated_at: 2023-02-02 00:00:00
tldr: Use the DataFrame.sort\_values() method, passing in a list of the desired column names to sort by as the first argument.
---

**Contents**

[TOC]

# Section 1: Import Libraries

In order to sort a dataFrame in Python Pandas by two or more columns, we need to first import the necessary libraries. The most important library we need is the Pandas library.

```python
import pandas as pd
```

# Section 2: Read Data

Next, we need to read the data into a dataFrame. We can do this by using the `read_csv()` function.

```python
df = pd.read_csv('data.csv')
```

# Section 3: Sort Data

Once we have the data in a dataFrame, we can use the `sort_values()` function to sort the data by two or more columns. For example, if we wanted to sort the data by the columns `Name` and `Age`, we would do the following:

```python
df.sort_values(by=['Name', 'Age'])
```

# Section 4: Output

Finally, we can output the sorted dataFrame by using the `to_csv()` function.

```python
df.to_csv('sorted_data.csv')
```
