---
title: Obtaining the row index within a pandas apply function
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-17 00:00:00
updated_at: 2023-04-17 00:00:00
tldr: The index of a row in a pandas apply function can be obtained using the `.name` attribute.
---

**Contents**

[TOC]

**Section 1: Introduction**

Pandas is a popular library in Python used for data manipulation and analysis. One of the key functionalities of the pandas library is its ability to apply functions to data. Pandas apply function allows a user to apply a function on either a row or column of a DataFrame. When applying a function to the rows of the DataFrame, there are times when a user may need to get the index of the currently selected row. This article will discuss how to get the index of a row in a Pandas apply function in Python.

**Section 2: The apply function**

The apply function is a method provided by the Pandas library to apply a function along an axis of a DataFrame. The apply function applies a function to either the rows or columns of the DataFrame. In most cases, the apply function is used to aggregate, transform or filter data. 

Here is an example of how to use the apply function to apply a lambda function to each row of a DataFrame:

``` python
import pandas as pd

df = pd.DataFrame({'A': [1, 2, 3], 'B': [4, 5, 6]})

df.apply(lambda row: row['A'] + row['B'], axis=1)

```

The code above applies a lambda function to each row of the DataFrame. The lambda function takes in a row as an argument and returns the sum of column A and column B. The axis parameter is set to 1 to indicate that we are applying the function to each row of the DataFrame.

**Section 3: Accessing row index**

To access the index of the row that is currently being processed, we can use the name attribute on the row object that is passed to the lambda function. The name attribute returns the index label of the specified row. Here is an example:

``` python
import pandas as pd

df = pd.DataFrame({'A': [1, 2, 3], 'B': [4, 5, 6]})

df.apply(lambda row: row.name, axis=1)

```

In this example, the lambda function returns the index label of each row in the DataFrame. The result of the apply function would be a Series object with the row index as the values.

**Section 4: Using enumerate to get both index and row data**

Besides using the name attribute on the row object, we can also use the built-in Python method called enumerate. The enumerate method allows us to get both the index and the data of a row being processed by the apply function. Here is an example:

``` python
import pandas as pd

df = pd.DataFrame({'A': [1, 2, 3], 'B': [4, 5, 6]})

df.apply(lambda row: (row.name, list(enumerate(row))), axis=1)

```

In this example, the lambda function returns a tuple of the index label and a list of tuples containing the column index and data of the row being processed. The result of the apply function would be a Series object with the tuple as the values.

**Conclusion**

Getting the index of a row being processed by the apply function in pandas is essential when working with data. We can use the name attribute of the row object or Python's built-in enumerate method to get the index label and data of a row being processed by the apply function.
