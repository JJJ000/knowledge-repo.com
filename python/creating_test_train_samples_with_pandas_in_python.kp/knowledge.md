---
title: What is the process for splitting a single dataframe into test and train samples using pandas?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-01 00:00:00
updated_at: 2023-02-01 00:00:00
tldr: You can use the train\_test\_split() function from the scikit-learn library to split a dataframe into train and test samples.
---

**Contents**

[TOC]

## Step 1: Create Train and Test Dataframes

Using the `pandas` library, you can create two dataframes, one for the training set and one for the test set. The `pandas.DataFrame()` function can be used to create a new dataframe from a given data set.

## Step 2: Split Data into Train and Test Sets

Once the two dataframes have been created, you can then use the `pandas.DataFrame.sample()` function to randomly select rows from the original dataframe and assign them to either the training or test dataframes. This can be done by specifying the fraction of the data that should be assigned to the training set and the fraction of the data that should be assigned to the test set.

## Step 3: Assign Labels

In order to use the data for training and testing, it is necessary to assign labels to the data. This can be done using the `pandas.DataFrame.assign()` function, which can be used to assign a label column to the dataframes.

## Step 4: Save Data

Finally, it is important to save the training and test dataframes to disk. This can be done using the `pandas.DataFrame.to_csv()` function, which can be used to save the dataframes to a comma-separated values (CSV) file.
