---
title: What is the difference between np.mean() and np.average() functions in Python numpy?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: Both functions calculate the mean of an array, but np.average() allows the user to assign weights to each element.
---

**Contents**

[TOC]

## Introduction
NumPy is a Python library that is widely used to perform mathematical and numerical operations. It includes a variety of useful functions for dealing with data, one of which is the ability to calculate an average or mean of a set of values. The NumPy library provides two functions for calculating these values, np.mean() and np.average(). This article will explore the differences between these two functions and the scenarios in which each is useful.

## np.mean()
The np.mean() function is a NumPy method that calculates the arithmetic mean of a given set of values. It simply adds all of the values in the array, and then divides the resulting sum by the total number of values. The result is a single value that represents the central tendency of the set of data. This function accepts an array or a list of numbers and can also work along a specific axis of the input array. If no axis is specified, the function calculates the mean of the entire array.

## np.average()
The np.average() function is another method present in the NumPy library that calculates the average of a given set of values. It has an optional argument called ‘weights’ that allows you to specify how much weight each value should have when calculating the average. The weighted average is calculated by multiplying each value by its corresponding weight, summing these products, and then dividing the resulting sum by the total weight. This feature makes the np.average() method more flexible than np.mean(), as you can assign different weights to different values, making it useful for working with grouped data or datasets with differing importance on values.

## Differences
The main difference between np.mean() and np.average() is that np.mean() calculates the simple average of all the values in an array whereas np.average() can be used to calculate a weighted average by assigning different weights to each value. Another difference between these two methods lies in their output. The np.mean() function always returns a floating-point number as a result. However, np.average() can return an array of different data type depending on the input array and specified axis.

## When to use np.mean() vs np.average()
The choice of which method to use largely depends on the type of data you are working with. If you have simple, unweighted data with no outliers, the np.mean() method should be used. If you are working with a set of data with varied importance or groups where you want to specify different weights to each group or value, the np.average() method should be used. Additionally, if you are dealing with non-numeric data, np.mean() may not be applicable.
