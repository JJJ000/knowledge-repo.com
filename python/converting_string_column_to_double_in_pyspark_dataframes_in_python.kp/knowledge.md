---
title: What is the process of converting a pyspark dataframe column from string data type to double data type?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-13 00:00:00
updated_at: 2023-03-13 00:00:00
tldr: Use the `cast` function on the column with the `DoubleType()` parameter.
---

**Contents**

[TOC]

## Step 1: Import required modules and create a PySpark session

``` python
from pyspark.sql.functions import col
from pyspark.sql.types import DoubleType
from pyspark.sql import SparkSession

# Create a SparkSession
spark = SparkSession.builder.appName("DataFrame String to Double Conversion").getOrCreate()
```

## Step 2: Create a sample dataframe with strings in one column

``` python
# Create a sample dataframe
data = [("John", "123.45"), ("Mike", "67.89"), ("Mary", "42.0")]
df = spark.createDataFrame(data, ["Name", "Marks"])
```

## Step 3: Convert the column from String to Double type using a user-defined function (UDF)

``` python
# Define a UDF to convert strings to doubles
toDouble = udf(lambda x: float(x), DoubleType())

# Apply the UDF to the "Marks" column
df = df.withColumn("Marks", toDouble(col("Marks")))
```

## Step 4: Verify the datatype of the dataframe column

``` python
# Verify the datatypes of the columns
df.printSchema()
```

Output:
```
root
 |-- Name: string (nullable = true)
 |-- Marks: double (nullable = true)
```

Note: The output confirms that the "Marks" column is now of DoubleType.
