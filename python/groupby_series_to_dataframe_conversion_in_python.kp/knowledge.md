---
title: Transforming a pandas groupby result from a series to a dataframe
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-01 00:00:00
updated_at: 2023-02-01 00:00:00
tldr: Use the reset\_index() method on the Series object to convert the GroupBy output from Series to DataFrame.
---

**Contents**

[TOC]

**Section 1: Overview**

Pandas GroupBy is a powerful tool for analyzing data in Python. It allows you to split a DataFrame into groups based on a certain criteria, and then apply a function to each group independently. The output of a GroupBy operation is a Series, but sometimes it is necessary to convert this Series into a DataFrame. This article will cover how to do this.

**Section 2: GroupBy Operation**

To demonstrate how to convert a GroupBy output from Series to DataFrame, let's first create a DataFrame and perform a GroupBy operation on it. For example, we can create a DataFrame of student grades, and then group the grades by student:

```python
import pandas as pd

# Create a DataFrame of student grades
df = pd.DataFrame({'Student': ['Alice', 'Bob', 'Charlie', 'Dave'], 
                   'Grade': [90, 85, 95, 80]})

# Group the grades by student
grouped = df.groupby('Student')['Grade'].mean()
```

The output of the GroupBy operation is a Series, as shown below:

```
Student
Alice     90
Bob       85
Charlie    95
Dave      80
Name: Grade, dtype: int64
```

**Section 3: Converting to DataFrame**

To convert the Series to a DataFrame, we can use the `to_frame()` method. This will create a DataFrame with a single column, which contains the values from the Series:

```python
# Convert the Series to a DataFrame
df_grouped = grouped.to_frame()
```

The resulting DataFrame will look like this:

```
       Grade
Student       
Alice       90
Bob         85
Charlie     95
Dave        80
```

**Section 4: Conclusion**

In this article, we covered how to convert a Pandas GroupBy output from Series to DataFrame. This can be done using the `to_frame()` method, which will create a DataFrame with a single column containing the values from the Series.
