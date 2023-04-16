---
title: What is the process for renaming columns in a pyspark dataframe?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: In PySpark, you can use the withColumnRenamed() method to change the column names of a dataframe.
---

**Contents**

[TOC]

### Section 1: Import Libraries

The following libraries need to be imported to change column names in a PySpark dataframe:

```python
from pyspark.sql.functions import col
```

### Section 2: Create DataFrame

To start, create a dataframe in PySpark with the following code:

```python
data = [('John', 25),('Bob', 22),('James', 28)]
df = spark.createDataFrame(data, schema=['Name', 'Age'])
df.show()
```

### Section 3: Change Column Names

To change the column names of the dataframe, use the following code:

```python
df = df.select(col('Name').alias('User_Name'), col('Age').alias('User_Age'))
df.show()
```

### Section 4: Check Column Names

To check the column names of the dataframe, use the following code:

```python
df.columns
```

The output should be: `['User_Name', 'User_Age']`
