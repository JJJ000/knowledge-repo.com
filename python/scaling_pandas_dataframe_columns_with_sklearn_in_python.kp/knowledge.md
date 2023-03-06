---
title: Reword using scikit-learn to scale columns in a pandas dataframe
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: We can use the `sklearn.preprocessing` module`s `StandardScaler()` or `MinMaxScaler()` function to scale columns of a pandas dataframe in Python.
---

**Contents**

[TOC]

Section 1: Introduction to pandas dataframe columns scaling

Scaling is an essential data preprocessing technique that is performed on numerical data during machine learning. It is done with the purpose to normalize the input variables to ensure that they have a similar range. Scaling is essential because some machine learning algorithms tend to behave poorly when the input variables have varying scales, magnitudes, or units. StandardScaler is a method in sklearn that scales the data in pandas dataframe columns in such a way that they have a mean of zero and a variance of one. In this article, we will discuss how to scale the pandas dataframe columns using StandardScaler.

Section 2: Data preparation 

Before scaling the columns, it is essential to prepare the data for processing. The data should be loaded in the pandas dataframe, and it should not contain any missing values. In case there are null values, they should be replaced with other statistics of that column such as mean, median, or mode.  

```
import pandas as pd

data = pd.read_csv('data.csv')
data.dropna(inplace=True) # drop rows with missing values
```

Section 3: Scaling the pandas dataframe columns 

After data preparation, we can now scale the pandas dataframe columns using StandardScaler. We exclude non-numeric columns such as categorical columns from scaling.

```
from sklearn.preprocessing import StandardScaler

num_cols = data.select_dtypes(include=['int64','float64']).columns.tolist() # get list of numeric columns
num_data = data[num_cols]    # get the numerical pandas dataframe 
scaler = StandardScaler()
scaled_data = scaler.fit_transform(num_data)
scaled_data_df = pd.DataFrame(scaled_data, columns=num_data.columns) # create pandas dataframe from scaled data
```

Section 4: Conclusion 

In conclusion, scaling the pandas dataframe columns using StandardScaler is essential in machine learning data preprocessing. We demonstrated how to prepare data, select numerical columns, scale them, and create a new pandas dataframe with the scaled columns. It is worth noting that other scaling techniques, such as MinMaxScaler and RobustScaler, can also be used depending on the nature of the data.
