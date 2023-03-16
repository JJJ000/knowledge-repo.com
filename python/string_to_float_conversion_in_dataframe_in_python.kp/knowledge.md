---
title: Transforming string values into decimal numbers within a dataframe
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-16 00:00:00
updated_at: 2023-03-16 00:00:00
tldr: You can convert a column of strings to floats in a DataFrame by applying the astype() method to the column.
---

**Contents**

[TOC]

Section 1: Introduction
In data analysis or data science, having clean and organized data is crucial for performing accurate and meaningful analyses. However, often, the data that we are working with may have some inconsistencies or errors. One common issue is the presence of string values when we need to work with float or numeric data types. In this tutorial, we will explore different methods to convert strings to floats in a pandas DataFrame in Python.

Section 2: Reading the Data
First, we need to read the data into a pandas DataFrame. Let's assume we have a CSV file with some string values that need to be converted to floats. We can read this CSV file using the pandas read_csv() function:

```
import pandas as pd

data = pd.read_csv('data.csv')
```

Section 3: Converting Strings to Floats
Now that we have our data in a pandas DataFrame, we can convert the string values to floats. There are several ways to do this, but one common method is to use the astype() method. This method allows us to convert the data type of a pandas Series or DataFrame.

```
data['column'] = data['column'].astype(float)
```

The above code converts the 'column' of the DataFrame to a float data type. We can also use the apply() method to apply the same operation to multiple columns of the DataFrame.

```
data[['column1', 'column2']] = data[['column1', 'column2']].apply(pd.to_numeric)
```

The above code converts the 'column1' and 'column2' of the DataFrame to a float data type.

Section 4: Handling Exceptions
Sometimes, the data may be inconsistent or contain some invalid values that cannot be converted to float values. In such cases, we can handle the exceptions using try-except blocks. The code below shows an example of how to handle such exceptions:

```
for i in range(len(data)):
    try:
        data.at[i, 'column'] = float(data.at[i, 'column'])
    except ValueError:
        data.at[i, 'column'] = None
```

The above code tries to convert each value of the 'column' to a float data type. If it fails to convert, it sets the value to None. We can then handle these None values later in our analysis.

Conclusion:
In this tutorial, we have explored different methods for converting strings to floats in a pandas DataFrame in Python. We have seen how to use the astype() method and apply() method to convert data types. We have also learned how to handle exceptions when the data contains invalid values.
