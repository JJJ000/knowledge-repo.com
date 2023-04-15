---
title: Comparison between applying and transforming operations on a group object
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-16 00:00:00
updated_at: 2023-04-16 00:00:00
tldr: The apply method applies a function to each column/row of a group object, while the transform method applies a function to each element of a group object.
---

**Contents**

[TOC]

Apply vs Transform on a Group Object in Python

When working with data frames, it is common to work with groups of data. Groupby() is a method in pandas that is used to group rows of data based on one or more columns. Once you have a groupby object, you can perform various operations on it using methods like apply() and transform(). In this article, we will explore the difference between the apply and transform methods on a groupby object in Python, and when to use which method.

Section 1: Understanding the Basics
Both apply() and transform() are methods that are used to perform operations on a groupby object in pandas. The basic difference between the two methods is that apply() returns a DataFrame, whereas transform() returns a Series or DataFrame.

Section 2: The Apply Method
The apply() method is used to apply a function to each group of a groupby object. The function can be any function that takes a DataFrame as input and returns a DataFrame. The apply() method then concatenates the output of the function for each group and returns a DataFrame with the same number of rows as the original DataFrame. 

Consider the following example:

```
import pandas as pd

data = {'Name': ['Tom', 'Jack', 'Carla', 'Ram', 'Max', 'Joe'], 
        'Group': ['A', 'B', 'A', 'B', 'A', 'A'], 
        'Score': [45, 84, 64, 91, 52, 97]}

df = pd.DataFrame(data)

grouped = df.groupby('Group')

def topN(df, n):
    return df.sort_values(by='Score', ascending=False)[:n]

print(grouped.apply(topN, n=2))
```

This code sorts each group by Score in descending order and returns the top two students from each group. The apply() method applies the function to each group and returns a DataFrame with the same number of rows as the original DataFrame.

Section 3: The Transform Method
The transform() method, on the other hand, applies a function to each group of a groupby object and returns a Series or DataFrame with the same number of rows as the original DataFrame. The output of the function is broadcasted to match the shape of the original DataFrame.

Consider the following example:

```
import pandas as pd

data = {'Name': ['Tom', 'Jack', 'Carla', 'Ram', 'Max', 'Joe'], 
        'Group': ['A', 'B', 'A', 'B', 'A', 'A'], 
        'Score': [45, 84, 64, 91, 52, 97]}

df = pd.DataFrame(data)

grouped = df.groupby('Group')

zscore = lambda x: (x - x.mean()) / x.std()

print(grouped.transform(zscore))
```

This code calculates the z-score of Score for each student within their respective group using the transform() method. The output is a DataFrame with the same number of rows as the original DataFrame.

Section 4: When to Use Which Method
The apply() method is useful when you want to apply a function to each group of a groupby object and return a DataFrame with the same number of rows as the original DataFrame. This is useful when you want to filter, sort or aggregate data within each group.

The transform() method is useful when you want to apply a function to each group of a groupby object and return a Series or DataFrame with the same number of rows as the original DataFrame. This is useful when you want to standardize data within each group, or when you want to fill missing values with the mean or median of each group.

In conclusion, both the apply() and transform() methods are useful for performing operations on a groupby object in pandas. The choice between the two depends on the type of output you need and the nature of the operation to be performed.
