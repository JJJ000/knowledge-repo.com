---
title: Select rows from the dataframe where the value in the specified column is one of the values in the given set
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-01 00:00:00
updated_at: 2023-02-01 00:00:00
tldr: Use the `isin()` method to filter dataframe rows if the value in a column is in a set list of values.
---

**Contents**

[TOC]

**Section 1 - Create a Set of Values**

A set of values can be created in Python by using the set() function. For example, the following code creates a set of values called "mySet":

```
mySet = set([1,2,3,4,5])
```

**Section 2 - Create a Dataframe**

A dataframe can be created in Python by using the pandas library. For example, the following code creates a dataframe called "myDataframe":

```
import pandas as pd 
myDataframe = pd.DataFrame({'A':[1,2,3,4,5], 'B':[6,7,8,9,10]})
```

**Section 3 - Filter Dataframe Rows**

The rows in the dataframe can be filtered based on the values in the column by using the isin() function. For example, the following code filters the rows in the dataframe based on the values in the column "A" and the set of values "mySet":

```
filteredDataframe = myDataframe[myDataframe['A'].isin(mySet)]
```

**Section 4 - Output Filtered Dataframe**

The filtered dataframe can be printed to the console by using the print() function. For example, the following code prints the filtered dataframe to the console:

```
print(filteredDataframe)
```
