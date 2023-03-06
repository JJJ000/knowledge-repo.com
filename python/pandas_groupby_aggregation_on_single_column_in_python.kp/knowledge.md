---
title: Pandas groupby.agg() function can be used to aggregate the same column in multiple ways
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: You can provide a list of aggregation functions to the agg() method when using pandas GroupBy, and each function will be applied to the same column.
---

**Contents**

[TOC]

Section 1: Introduction
When performing data analysis, it's not uncommon to want to compute multiple aggregations over the same column or set of columns. In pandas, this can be achieved using the GroupBy.agg() method. In this tutorial, we'll walk through how to use this method to perform multiple aggregations of the same column.

Section 2: Syntax of GroupBy.agg()
The GroupBy.agg() method allows you to perform multiple aggregations on one or more columns. The syntax for this method is as follows:

```
df.groupby('column_name').agg({'column_name': ['aggregation_function1', 'aggregation_function2', ...]})
```

Here, the `groupby()` method is used to group the DataFrame by the desired column, and the `agg()` method is used to specify the column(s) and the aggregation functions to apply. Note that the column name(s) to apply the aggregations must be specified in a dictionary where the keys are the column name(s) and the values are a list of the aggregation functions to be applied.

Section 3: Example
Let's work with an example to understand how to use GroupBy.agg() to perform multiple aggregations over the same column. Suppose we have a DataFrame that looks like this:

```
import pandas as pd

data = {'name': ['Alice', 'Bob', 'Charlie', 'Alice', 'Bob', 'Charlie'],
        'score': [90, 85, 95, 92, 88, 93],
        'age': [25, 30, 27, 25, 30, 27]}

df = pd.DataFrame(data)
```

Our goal is to group the DataFrame by the 'name' column and compute the mean and standard deviation of the 'score' column for each group. We can do this using GroupBy.agg() as follows:

```
result = df.groupby('name').agg({'score': ['mean', 'std']})
```

This will result in a new DataFrame that looks like this:

```
           score          
            mean       std
name                      
Alice  91.000000  1.414214
Bob    86.500000  2.121320
Charlie 94.000000  1.414214
```

As you can see, the 'score' column has been aggregated using the mean and standard deviation functions, resulting in a new DataFrame with two columns: 'mean' and 'std'.

Section 4: Conclusion
In summary, GroupBy.agg() in pandas can be used to perform multiple aggregations of the same column. By specifying the column(s) and the aggregation functions to apply in a dictionary, we can compute various statistics for each group in a DataFrame. This can be useful for analyzing and summarizing data sets.
