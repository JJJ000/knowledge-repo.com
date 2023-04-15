---
title: How to screen a pyspark dataframe column that has a none value?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: To filter a Pyspark dataframe column with None value in Python, use `.isNull()` function on the desired column.
---

**Contents**

[TOC]

# Introduction

In this tutorial, we will learn how to filter PySpark dataframe column with None value in Python. PySpark is a popular framework used for big data processing and analysis. It is a distributed computing engine that provides efficient processing of large datasets. PySpark uses Apache Spark as its backend engine and provides an easy-to-use Python API for working with Spark. Dataframes are one of the key data structures in PySpark that provides an efficient way to store and process large datasets. In this tutorial, we will use PySpark dataframes to filter the columns with None value.


# Example Data

We will use the following example data for this tutorial. 


| name   | age | city     |
|-------|-----|----------|
| Alice | 25  | New York |
| Bob   | 30  | London   |
| Carol | 35  | None     |
| Dave  | 40  | Paris    |
| Eve   | 45  | None     |
| Finn  | 50  | Berlin   |


# Filtering PySpark Dataframe Column with None Value

PySpark dataframes provide a number of functions to filter columns with None values. We can use the `isNull()` or `isNotNull()` function to filter the column with None or non-None values, respectively.

The following code snippet shows how to filter the `city` column of the above PySpark dataframe with None values:

```python
from pyspark.sql.functions import isnull

# read the data into a PySpark dataframe
df = spark.read.csv('example.csv', header=True)

# filter the city column with None values
result = df.filter(isnull(df.city))

# show the result
result.show()
```

Output:
```
+-----+---+----+
| name|age|city|
+-----+---+----+
|Carol| 35|null|
|  Eve| 45|null|
+-----+---+----+
```

Similarly, we can filter the column with non-None values using the `isNotNull()` function:

```python
from pyspark.sql.functions import isnotnull

# filter the city column with non-None values
result = df.filter(isnotnull(df.city))

# show the result
result.show()
```

Output:
```
+-----+---+--------+
| name|age|    city|
+-----+---+--------+
|Alice| 25|New York|
|  Bob| 30|  London|
| Dave| 40|   Paris|
| Finn| 50|  Berlin|
+-----+---+--------+
```


# Conclusion

In this tutorial, we learned how to filter PySpark dataframe column with None value in Python. We used `isNull()` and `isNotNull()` functions to filter the column with None and non-None values, respectively. PySpark dataframes provide an efficient way to work with large datasets and can be easily integrated with other big data technologies.
