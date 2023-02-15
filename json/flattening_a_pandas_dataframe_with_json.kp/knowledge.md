---
title: What is the best way to convert a pandas dataframe with some columns as JSON into a single-level dataframe?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-15 00:00:00
updated_at: 2023-02-15 00:00:00
tldr: Use the json\_normalize() function to flatten a pandas dataframe with some columns as json.
---

**Contents**

[TOC]

### 1. Load the Data

First, we need to load the data into a Pandas dataframe. This can be done using the `pd.read_csv()` function.

### 2. Convert JSON Columns

Next, we need to convert the columns with JSON data into a flattened format. This can be done using the `json_normalize()` function. This function takes in the JSON data as a string and returns a flattened dataframe.

### 3. Merge Dataframes

Once the JSON columns have been converted to a flattened dataframe, we can merge the two dataframes together using the `pd.concat()` function. This will combine the two dataframes into a single dataframe with all of the columns from both.

### 4. Clean Up Data

Finally, we need to clean up the data to remove any duplicate columns or rows. This can be done using the `df.drop_duplicates()` function. This will remove any duplicate columns or rows from the dataframe.
