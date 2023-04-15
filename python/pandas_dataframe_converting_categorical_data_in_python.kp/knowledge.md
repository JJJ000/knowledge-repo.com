---
title: Reword 'transform categorical information within a pandas data table.'
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Categorical data in pandas dataframe can be converted using the `astype` method or the `category` datatype in pandas.
---

**Contents**

[TOC]

## Method 1: Pandas' get_dummies()

Pandas provides a method called `get_dummies()` to convert categorical data into numerical data. This method creates binary columns for each category by splitting the categorical column. Each row will have a 1 for the category it belongs to and 0 for all other categories.

```python
import pandas as pd

# create a sample dataframe
df = pd.DataFrame({'fruits': ['apple', 'banana', 'orange', 'apple', 'orange', 'banana']})

# get dummies
df_dummies = pd.get_dummies(df['fruits'])

# concatenate dummies dataframe with original dataframe
df_concat = pd.concat([df, df_dummies], axis=1)

print(df_concat)
```
Output:
```
    fruits  apple  banana  orange
0    apple      1       0       0
1   banana      0       1       0
2   orange      0       0       1
3    apple      1       0       0
4   orange      0       0       1
5   banana      0       1       0
```

## Method 2: Label Encoding with Scikit-Learn

Scikit-Learn library provides a method called `LabelEncoder()` to convert categorical data to numerical data by assigning numbers to each category. The numbers are assigned based on the alphabetical order of categories.

```python
from sklearn.preprocessing import LabelEncoder

# create a sample dataframe
df = pd.DataFrame({'fruits': ['apple', 'banana', 'orange', 'apple', 'orange', 'banana']})

# create an instance of LabelEncoder
lbl_enc = LabelEncoder()

# fit and transform the categorical column
df['fruits_lbl'] = lbl_enc.fit_transform(df['fruits'])

print(df)
```
Output:
```
   fruits  fruits_lbl
0   apple           0
1  banana           1
2  orange           2
3   apple           0
4  orange           2
5  banana           1
```

## Method 3: One-Hot Encoding with Scikit-Learn

One-Hot Encoding is another method to convert categorical data into numerical data. Scikit-Learn's `OneHotEncoder()` method creates a binary column for each category just like `get_dummies()` method of Pandas. One minor difference is that OneHotEncoder() returns a sparse matrix by default. The sparse matrix has many 0s, which makes the transformation efficient but occupies less memory.

```python
from sklearn.preprocessing import OneHotEncoder

# create a sample dataframe
df = pd.DataFrame({'fruits': ['apple', 'banana', 'orange', 'apple', 'orange', 'banana']})

# create an instance of OneHotEncoder
ohe = OneHotEncoder(sparse=False)

# fit and transform the categorical column
df_ohe = ohe.fit_transform(df[['fruits']])

# create a dataframe with the transformed data
df_ohe = pd.DataFrame(df_ohe, columns=ohe.get_feature_names())

# concatenate the transformed dataframe with the original dataframe
df_concat = pd.concat([df, df_ohe], axis=1)

print(df_concat)
```
Output:
```
   fruits    x0_apple  x0_banana  x0_orange
0   apple           1          0          0
1  banana           0          1          0
2  orange           0          0          1
3   apple           1          0          0
4  orange           0          0          1
5  banana           0          1          0
```


## Method 4: Custom Mapping

Custom Mapping is another way to convert categorical data by mapping the categories with custom numerical values.

```python
# create a sample dataframe
df = pd.DataFrame({'fruits': ['apple', 'banana', 'orange', 'apple', 'orange', 'banana']})

# create a dictionary with custom mapping
mapping = {'apple': 1, 'banana': 2, 'orange': 3}

# map the categorical column
df['fruits_map'] = df['fruits'].map(mapping)

print(df)
```
Output:
```
   fruits  fruits_map
0   apple           1
1  banana           2
2  orange           3
3   apple           1
4  orange           3
5  banana           2
```
