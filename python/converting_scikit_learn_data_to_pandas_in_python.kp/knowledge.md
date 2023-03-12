---
title: What is the process of transforming a scikit-learn dataset into a pandas dataset?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-12 00:00:00
updated_at: 2023-03-12 00:00:00
tldr: Use the Pandas DataFrame function to convert the Scikit-learn dataset to a Pandas dataset.
---

**Contents**

[TOC]

Section 1: Introduction
In this tutorial, we will learn how to convert a scikit-learn dataset to a Pandas dataset in Python. Scikit-learn is a powerful Python module for machine learning, while pandas is a fast, powerful, flexible, and easy-to-use data analysis and manipulation tool which helps in data manipulation and analysis. Often, we may need to convert a dataset to or from scikit-learn to pandas so that it is easier to work with the data irrespective of whether we want to do data analysis or machine learning.

Section 2: Loading the scikit-learn dataset
Before converting the dataset to pandas, we first need to load the scikit-learn dataset that we want to convert.  Scikit-learn provides a number of sample datasets for testing and experimentation, in addition to several standard datasets used for various machine learning tasks. For this tutorial, we will use the iris dataset from sklearn. 

```python
    from sklearn import datasets

    iris = datasets.load_iris()  # load the iris dataset
```

Section 3: Converting scikit-learn dataset to Pandas dataset
Once we have loaded the dataset, we can easily convert it to a pandas dataset using the pandas.DataFrame() method. This method can take a dictionary as an argument, with the keys being the names of the columns and the values being the data points. We can get the column names from the "feature_names" attribute of iris dataset, which is a list containing the names of the four features of the dataset. We can then add the target column to the dictionary as well.

```python
    import pandas as pd

    # convert to pandas dataset
    iris_df = pd.DataFrame(data=iris['data'], columns=iris['feature_names'])
    iris_df['target'] = iris['target']
```

Section 4: Conclusion
In this tutorial, we learned how to convert a scikit-learn dataset to a pandas dataset in Python using the pandas.DataFrame() method. This can be useful in cases where we want to manipulate or analyze data, or use scikit-learn functions on the dataset without using the scikit-learn API.
