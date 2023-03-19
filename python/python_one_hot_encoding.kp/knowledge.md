---
title: What is the method for one hot encoding in python?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: Use the `OneHotEncoder` class from the `sklearn.preprocessing` module to perform one hot encoding in Python.
---

**Contents**

[TOC]

## Introduction
One hot encoding is a process of converting categorical data into a binary format that can be used in machine learning algorithms. In this technique, each category of a feature is represented as a binary vector, where each dimension of the vector corresponds to a category.

## Method

There are several ways to one hot encode in Python, but we will demonstrate two methods: using Pandas and Scikit-learn.

### Method 1: Using Pandas
Pandas provides a function called `get_dummies()` that can be used to one hot encode a feature. Here’s an example:

``` python
import pandas as pd

data = {'fruit': ['apple', 'banana', 'orange', 'banana', 'apple']}
df = pd.DataFrame(data)

# One hot encode the fruit column
one_hot = pd.get_dummies(df['fruit'])

# Join the one hot encoded data with the original data frame
df = df.join(one_hot)
```

### Method 2: Using Scikit-learn
Scikit-learn provides a class called `OneHotEncoder` that can be used to one hot encode a feature. Here’s an example:

``` python
from sklearn.preprocessing import OneHotEncoder
import numpy as np

data = np.array(['apple', 'banana', 'orange', 'banana', 'apple']).reshape(-1,1)

# Instantiate the encoder
encoder = OneHotEncoder(sparse=False)

# Fit and transform the data
one_hot = encoder.fit_transform(data)

# Print the result
print(one_hot)
```

## Conclusion
One hot encoding is an important technique for converting categorical data into a format that can be used in machine learning algorithms. Both Pandas and Scikit-learn provide easy-to-use methods for one hot encoding in Python.
