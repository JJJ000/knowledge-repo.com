---
title: Interpret a column of JSON strings using pyspark
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Use the built-in from\_json() function to parse a column of JSON strings in PySpark.
---

**Contents**

[TOC]

### Section 1: Create DataFrame

To parse a column of JSON strings, the first step is to create a DataFrame. This can be done by using the `read.json` method in the `pyspark.sql.DataFrameReader` class. The `read.json` method takes a path to the JSON file as an argument and creates a DataFrame with the column data.

### Section 2: Parse JSON String

Once the DataFrame is created, the JSON string can be parsed using the `from_json` method. The `from_json` method takes the JSON string as an argument and returns a column of data.

### Section 3: Extract Columns

The parsed column of data can then be used to extract the desired columns. This can be done by using the `select` method in the `pyspark.sql.DataFrame` class. The `select` method takes a list of column names as an argument and returns a DataFrame with only the specified columns.

### Section 4: Save DataFrame

Once the desired columns have been extracted, the DataFrame can be saved to a file. This can be done by using the `write.csv` method in the `pyspark.sql.DataFrameWriter` class. The `write.csv` method takes a path to the output file as an argument and saves the DataFrame to the specified file.
