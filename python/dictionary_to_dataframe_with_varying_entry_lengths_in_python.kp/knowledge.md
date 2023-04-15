---
title: Generating a dataframe through a dictionary containing entries of varying lengths
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-18 00:00:00
updated_at: 2023-04-18 00:00:00
tldr: Use the pandas DataFrame constructor with the dictionary and specify the longest entry`s length as the number of rows, filling shorter entries with NaN values.
---

**Contents**

[TOC]

Section 1: Introduction 

In Python, a dictionary is a collection of key-value pairs where each key is unique. A key-value pair is a set of two linked data items where the key is used to access the corresponding value. In this scenario, we will explore how to create a dataframe from a dictionary where entries have different lengths. A pandas dataframe is a two-dimensional, size-mutable, and heterogeneous tabular data structure that allows for the storage and manipulation of labeled data. This is a common occurrence in the real world, where datasets usually come with missing or additional information, which makes it challenging to manipulate them effectively. Fortunately, using pandas, we can handle this problem by creating dataframes that can handle missing or additional data.

Section 2: Creating a dictionary with different lengths

To create a dictionary with different lengths, we need to use a loop to iterate over each key-value pair and add it to the dictionary. To illustrate this, let's create a dictionary with different length values.

```
dictionary = {'A': [4,6,8], 'B': [7,4,9,5], 'C': [1,2]}
```

In this example, we have three keys and three lists of different sizes. Key 'A' has a list with three values, Key 'B' has a list with four values, and Key 'C' has a list with two values.

Section 3: Creating a pandas dataframe from a dictionary with different lengths

To create a pandas dataframe from a dictionary with different lengths, we will first import pandas and create a pandas dataframe using the from_dict function. The from_dict function allows us to create a dataframe from a dictionary. Additionally, we will use the orient parameter set to 'index' to specify that we want to create a dataframe using dictionary keys as row labels. Here's the code:

```
import pandas as pd

dictionary = {'A': [4,6,8], 'B': [7,4,9,5], 'C': [1,2]}

df = pd.DataFrame.from_dict(dictionary, orient='index')
```

In this code fragment, we created a pandas dataframe from the dictionary where the keys are row labels. Notice that pandas automatically filled the missing values with NaN.

Section 4: Conclusion

In this tutorial, we learned how to create a dictionary with different lengths and how to create a pandas dataframe from it. In real-life scenarios, datasets usually have incomplete data, which makes data wrangling challenging. But now, with pandas, we can handle missing or additional data effectively. This skill is essential for any data scientist, machine learning engineer, or person who deals with data regularly.
