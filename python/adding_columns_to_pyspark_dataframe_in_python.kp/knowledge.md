---
title: What is the process of adding a new column to a spark dataframe, and how can this be achieved using pyspark?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-18 00:00:00
updated_at: 2023-04-18 00:00:00
tldr: Use the withColumn method to add a new column to a Spark DataFrame in PySpark.
---

**Contents**

[TOC]

## Introduction
A DataFrame in Spark is a distributed collection of data organized into columns. Each column in a DataFrame is a series of data, while a complete DataFrame is a collection of data organized in rows and columns. To add a column to an existing DataFrame, we can use PySpark's `withColumn()` method. This method allows us to create a new column by executing an expression on the data held in the DataFrame.

### Step 1: Create a Spark DataFrame
To demonstrate how to add a new column to a Spark DataFrame using PySpark, let's first create a DataFrame. In the code snippet below, we will create a simple DataFrame with two columns - `name` and `age`.

```Python
from pyspark.sql import SparkSession
spark = SparkSession.builder.appName('NewColumnApp').getOrCreate()

data = [('Alice', 25), ('Bob', 22), ('Charlie', 30)]
columns = ['name', 'age']
df = spark.createDataFrame(data=data, schema=columns)
df.show()
```
The output of the above snippet will create a DataFrame - 
```
+-------+---+
|   name|age|
+-------+---+
|  Alice| 25|
|    Bob| 22|
|Charlie| 30|
+-------+---+
```

### Step 2: Add a new column to the DataFrame
We can use the `withColumn()` method to add a new column to the existing DataFrame. The `withColumn()` method requires two arguments:
- Name of the new column that we want to create.
- An expression to populate the values of the new column. This expression is executed on the data held in the DataFrame and returns a new column.

In the following code, we will add a new column - **`gender`** to the existing DataFrame using the PySpark's `withColumn()` method.

```Python
from pyspark.sql.functions import when

df = df.withColumn('gender', when(df.name=='Charlie', 'male').otherwise('female'))
df.show()
```
The output of above code snippest will be - 
```
+-------+---+------+
|   name|age|gender|
+-------+---+------+
|  Alice| 25|female|
|    Bob| 22|female|
|Charlie| 30|  male|
+-------+---+------+
```
In the above code snippet, we have used `when()` method to identify which name holds 'Charlie' and then assign gender as 'male' to this row. For all other rows, gender is assigned to 'female' using `otherwise()` method.

### Step 3: Drop an existing column
We can use PySpark's `drop()` method to remove an existing column from a DataFrame. In the following code, we will demonstrate how to remove the age column from the DataFrame.

```Python
df = df.drop('age')
df.show()
```
The output of above code snippest will be - 
```
+-------+------+
|   name|gender|
+-------+------+
|  Alice|female|
|    Bob|female|
|Charlie|  male|
+-------+------+
```

### Step 4: Rename an existing column
We can use the `withColumnRenamed()` method to rename an existing column in a PySpark DataFrame. In the following code, we will rename the **`gender`** column to **`sex`**.

```Python
df = df.withColumnRenamed('gender', 'sex')
df.show()
```
The output of above code snippest will be - 
```
+-------+----+
|   name| sex|
+-------+----+
|  Alice|female|
|    Bob|female|
|Charlie| male|
+-------+----+
```

## Conclusion
In this tutorial, we have learned how to add a new column to a PySpark DataFrame using the `withColumn()` method. We have also learned how to remove an existing column using the `drop()` method and rename an existing column using the `withColumnRenamed()` method.
