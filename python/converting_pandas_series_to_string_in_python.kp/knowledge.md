---
title: Change the data type of a pandas series to a string
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: To change data type of a Series to string in Pandas, use the `.astype(str)` method.
---

**Contents**

[TOC]

Section 1: Introduction to Pandas Series
========================================
Pandas is an open-source library in Python that is popularly used for data manipulation and analysis. It provides a powerful data structure called Series that can store data of different types, such as int, float, datetime, and string. In this tutorial, we will see how to change the data type of a Pandas Series to string in Python.

Section 2: Creating a Pandas Series
==================================
To demonstrate how to change the data type of a Pandas Series to string, we need to create a Series first. We can create a Series from a list, a tuple, a dictionary, or from a NumPy array.

```python
import pandas as pd

# Create a list of numbers
data = [1, 2, 3, 4, 5]

# Create a Pandas Series from the list
s = pd.Series(data)

# Print the original Series
print(s)
```
Output:
```
0    1
1    2
2    3
3    4
4    5
dtype: int64
```

Section 3: Changing the Data Type of a Pandas Series to String
==============================================================
To change the data type of a Pandas Series to string, we can use the `astype()` method. This method returns a copy of the Series with the specified data type. We can pass `str` as an argument to this method to convert the Series to a string data type.

```python
# Convert the Series to a string data type
s = s.astype(str)

# Print the modified Series
print(s)
```
Output:
```
0    1
1    2
2    3
3    4
4    5
dtype: object
```

Note that the data type of the Series has changed to `object`, which is the data type used to represent strings in Pandas.

Section 4: Conclusion
======================
In this tutorial, we saw how to change the data type of a Pandas Series to string in Python. We used the `astype()` method to convert the Series to a string data type. The method returns a copy of the modified Series, which we can use as per our requirements.
