---
title: Transform a column of a spark dataframe to a Python list
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-12 00:00:00
updated_at: 2023-03-12 00:00:00
tldr: Use the collect() method on the DataFrame column and convert it to a Python list.
---

**Contents**

[TOC]

## Method 1: Using "collect()" and "tolist()"

The first method to convert a Spark DataFrame column to a Python list is by using the "collect()" method of Spark DataFrame, and then convert the collected column data to a Python list using the "tolist()" method of the NumPy array.

```python
import numpy as np

# Assuming spark_df is the Spark DataFrame
column_data = spark_df.select("<column_name>").rdd.flatMap(lambda x: x).collect()
python_list = np.array(column_data).tolist()
```

## Method 2: Using "toPandas()" and "tolist()"

The second method is to convert a Spark DataFrame column to a Python list is by first converting the entire Spark DataFrame to a Pandas DataFrame using "toPandas()", and then convert the desired column in the Pandas DataFrame to a Python list using "tolist()".

```python
# Assuming spark_df is the Spark DataFrame
pandas_df = spark_df.toPandas()
python_list = pandas_df["<column_name>"].tolist()
```

## Method 3: Using List Comprehension

The third method is to use list comprehension to extract the values from the desired column of the input Spark DataFrame.

```python
# Assuming spark_df is the Spark DataFrame
python_list = [item[0] for item in spark_df.select("<column_name>").collect()]
```

## Method 4: Using RDD's map() function

The fourth method is to use the RDD's map() function to extract the values from the desired column of the input Spark DataFrame.

```python
# Assuming spark_df is the Spark DataFrame
python_list = spark_df.select("<column_name>").rdd.map(lambda x: x[0]).collect()
```
