---
title: Can you clarify the dissimilarity between 'transform' and 'fit_transform' in sklearn?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-08 00:00:00
updated_at: 2023-03-08 00:00:00
tldr: `transform` is used to apply a transformation to a dataset, while `fit\_transform` is used to both fit a transformation to the training data and apply it to the dataset.
---

**Contents**

[TOC]

## Fit

The `fit` method is used to train a machine learning model on a given dataset. During this process, the model tries to capture the patterns and relationships between the input features and the output variable. Once the model is trained, it can be used to make predictions on new data.

## Transform

The `transform` method is used to apply a specific transformation to a dataset. This could include scaling the data, encoding categorical variables, or feature engineering. 

## fit_transform

The `fit_transform` method is a combination of the `fit` and `transform` methods. It is used to both train a model on a given dataset and apply a specific transformation to that dataset at the same time. This can be useful when the transformation requires information from the training dataset in order to be applied correctly, such as with feature scaling. 

In summary, `fit` is used for training a model, `transform` is used for applying a transformation to a dataset, and `fit_transform` is a combination of the two for when training and transformation are done together.
