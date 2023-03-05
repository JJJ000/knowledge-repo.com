---
title: Substitute nan values in a pandas dataframe with the column average
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-05 00:00:00
updated_at: 2023-03-05 00:00:00
tldr: You can replace NaN values in a pandas DataFrame with the column averages using the fillna() method with the mean() function as the argument.
---

**Contents**

[TOC]

Section 1: Introduction
-----------------------
In this task, we will be discussing how to replace NaN values with the average of columns in a pandas DataFrame in Python. NaN values are missing or null values in the dataset. These values can affect the analysis or modeling of the dataset. Therefore, we need to replace them with appropriate values such as the average of columns. Pandas provide various functions to handle missing values. We will use the fillna() and mean() functions to accomplish the task at hand.

Section 2: Load the data and check for missing values

```
import pandas as pd
import numpy as np

# Load the dataset
df = pd.read_csv('data.csv')

# Check for missing values in the dataset
print(df.isnull().sum())
```

In this section, we import the necessary libraries and load the dataset into a DataFrame using the read_csv() function in pandas. We then check for missing values in the dataset using the isnull() function. This function returns a DataFrame containing True for missing values and False for non-missing values. We then use the sum() function to count the number of missing values in each column.

Section 3: Replace missing values with column average

```
# Replace the missing values with the column average
df = df.fillna(df.mean())
```

In this section, we replace the missing values in the DataFrame with the average value of each column using the fillna() function. We pass the mean value of the columns to the fillna() function to replace the missing values. The mean() function calculates the average of each column, and we assign the returned DataFrame to the original DataFrame 'df'.

Section 4: Verification of missing values

```
# Verify if the missing values were replaced with the column average
print(df.isnull().sum())
```

In this section, we check once again the updated DataFrame for any missing values. We use the isnull() and sum() functions as before to count the number of missing values in each column. If the count is zero, then there are no missing values in the DataFrame. If there are still missing values, we can repeat the process with a different technique to handle missing values.


Conclusion
-----------
In this task, we demonstrated how to replace missing values in a pandas DataFrame with the column average. We used the fillna() and mean() functions to perform the task. By replacing the missing values with appropriate values, we can make the analysis and modeling of the dataset more accurate and robust.
