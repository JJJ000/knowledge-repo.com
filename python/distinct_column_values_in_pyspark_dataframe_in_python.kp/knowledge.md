---
title: Display unique values for each column in pyspark dataframe
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-08 00:00:00
updated_at: 2023-03-08 00:00:00
tldr: To show distinct column values in a PySpark dataframe in Python, use the `distinct()` method on the column of interest.
---

**Contents**

[TOC]

# Introduction
In this tutorial, I will show you how to display distinct values of a specific column in a PySpark DataFrame.

# Sample Data
Suppose we have a PySpark DataFrame named `df` that contains the following data:

```
+----+------+
| id | name |
+----+------+
| 1  | John |
| 2  | Mary |
| 3  | John |
| 4  | Adam |
| 5  | Mary |
+----+------+
```

# Display distinct values of a specific column

To display the distinct values of a specific column in PySpark DataFrame, you can use the `distinct()` method on the column. Here's how you can do it:

```python
# import necessary libraries
from pyspark.sql.functions import col

# display distinct values of the name column
df.select(col("name")).distinct().show()
```

Output:
```
+-----+
| name|
+-----+
| John|
| Adam|
| Mary|
+-----+
```

# Save distinct column values to a new variable

If you want to save the distinct column values to a new variable, you can use the `collect()` method in addition to the `distinct()` method. Here's how:

```python
# create a new variable to store distinct column values
distinct_names = [row[0] for row in df.select(col("name")).distinct().collect()]
print(distinct_names)
```

Output:
```
['John', 'Adam', 'Mary']
```


# Conclusion
In this tutorial, we showed how to display the distinct values of a specific column in a PySpark DataFrame and how to save these distinct values to a new variable. This is a useful technique to use when you need to analyze a PySpark DataFrame and get unique information from it.
