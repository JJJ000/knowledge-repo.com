---
title: The error 'valueerror input contains nan, infinity or a value that exceeds the dtype('float64') limit' occurred in sklearn
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: The NaN, infinity or a value too large for dtype(`float64`) error in sklearn occurs when there are missing or invalid values in the input dataset.
---

**Contents**

[TOC]

Introduction
-------------

Python is one of the most popular open-source programming languages used for machine learning applications. There are many libraries available in Python to work with machine learning, including scikit-learn (sklearn), TensorFlow, and PyTorch. Among these libraries, scikit-learn is one of the most widely used libraries. sklearn's purpose is to make it easy for developers to implement various machine learning algorithms. However, sometimes you might encounter an error message like the following when using sklearn:

ValueError: Input contains NaN, infinity or a value too large for dtype('float64')

This error message indicates that the input data passed to the function contains missing or undefined values, as well as infinity or extremely large values. In this article, we'll explore the cause of the error and possible solutions.

Causes of the Error
---------------------

The ValueError: Input contains NaN, infinity or a value too large for dtype('float64') error usually occurs when the input data passed to a function contains NaN (Not a Number) or infinite values. For instance, if you read a CSV file using the pandas library and then try to use that data to train a machine learning model in sklearn, missing or undefined values in the CSV file can cause this error.

Another scenario that can cause this error is when the input data is not properly normalized, in which case the input data can contain values that are too large for dtype('float64').

Solutions to the Error
------------------------

1.   Check Your Input Data
     -----------------------
     
The first solution is to check your input data for missing or undefined values. You can do this by opening the input data in a text editor and carefully reading through it to identify any missing or undefined values. Alternatively, you can use tools such as pandas to read your data, then call the .isnull() method to check for any missing values.

2.   Replace Missing Values
     -----------------------
     
Once you have identified any missing values in your input data, the next step is to replace them with appropriate values. For instance, you can replace missing values with the mean or median of the non-missing values in the same column. There are several ways to do this in Python, including using pandas' fillna() method, numpy's replace() method, or sklearn's SimpleImputer().

3.   Normalize Your Input Data
     ---------------------------
     
Normalization is a technique often used to scale input data to the same range, which typically improves the performance of machine learning models. Sklearn provides a few normalization techniques, such as MinMaxScaler or StandardScaler. By scaling your input data, you can avoid the ValueError: Input contains NaN, infinity, or a value too large for dtype('float64') error caused by unnormalized inputs.

4.   Use Model-Based Imputation
     ---------------------------
     
Sklearn provides several classes that implement imputation algorithms (SimpleImputer, KNNImputer, IterativeImputer, and BayesianRidge), which can be used as part of the machine learning model fitting process. You can choose an appropriate imputation algorithm based on the distribution and nature of your data. The advantage of these techniques is that they are optimized for imputing data for a specific estimator. For instance, if KNN is your preferred algorithm, then KNNImputer would be a natural choice.

Conclusion
-----------

In conclusion, the ValueError: Input contains NaN, infinity, or a value too large for dtype('float64') error is caused by invalid or missing input data, which can often be fixed by replacing missing values with valid values, normalizing input data, or using appropriate imputation techniques. These solutions ensure that the input data is suitable for use with scikit-learn's various machine learning algorithms, enabling developers to build powerful and accurate machine learning models.
