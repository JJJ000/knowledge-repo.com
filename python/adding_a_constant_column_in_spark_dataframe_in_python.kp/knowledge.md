---
title: What is the process of adding a constant column in a spark dataframe?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-07 00:00:00
updated_at: 2023-03-07 00:00:00
tldr: Use the `withColumn` method to add a new column with a constant value to a Spark DataFrame.
---

**Contents**

[TOC]

## Creating a Spark DataFrame

First, we need to create a Spark DataFrame that we will use for our example. We can create a DataFrame using a list of tuples, where each tuple represents a row. Each tuple should have the same number of elements as the number of columns in the DataFrame. For this example, we'll create a DataFrame with two columns: `name` and `age`.

```python
from pyspark.sql import SparkSession

spark = SparkSession.builder.appName("Constant Column Example").getOrCreate()

data = [("Alice", 25), ("Bob", 30), ("Charlie", 35)]
df = spark.createDataFrame(data, ["name", "age"])
```

## Adding a Constant Column to the DataFrame

To add a constant column to the DataFrame, we can use the `withColumn` method. This method takes two parameters: the name of the new column (as a string) and the column definition (which can be an expression, a function that takes a row as input, or a literal value). In our case, we'll use a literal value for the constant column.

```python
from pyspark.sql.functions import lit

df_with_constant = df.withColumn("salary", lit(50000))
```

The `lit` function is used to create a new column with a constant value of `50000`.

## Displaying the DataFrame

We can display the original DataFrame and the new DataFrame (with the constant column) to verify that the constant column was added correctly.

```python
df.show()
df_with_constant.show()
```

The output should be:

```
+-------+---+
|   name|age|
+-------+---+
|  Alice| 25|
|    Bob| 30|
|Charlie| 35|
+-------+---+

+-------+---+------+
|   name|age|salary|
+-------+---+------+
|  Alice| 25| 50000|
|    Bob| 30| 50000|
|Charlie| 35| 50000|
+-------+---+------+
```

## Conclusion

In this example, we saw how to add a constant column to a Spark DataFrame in Python using the `withColumn` method and the `lit` function. This technique can be used to add columns with other constant values or to create columns based on more complex expressions or functions.
