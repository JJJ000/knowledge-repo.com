---
title: What is the method to format the columns of a pandas dataframe that contains floats?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-16 00:00:00
updated_at: 2023-04-16 00:00:00
tldr: Use the DataFrame.style.format() method along with the appropriate format string to display pandas DataFrame of floats using a format string for columns in Python.
---

**Contents**

[TOC]

# Introduction

Pandas is a very popular library in Python for data manipulation and analysis. It is widely used for reading different formats of data and storing them as DataFrames. Sometimes, we might want to display DataFrames with certain formats like floats. In this tutorial, we will learn how to display DataFrames of floats using a format string for columns in Python.

## Importing Required Libraries

Before we start with the main part of the tutorial, we need to import the required libraries. We will be using the pandas library to read and manipulate the data and the numpy library to generate random data.

``` python
import pandas as pd
import numpy as np
```

## Creating a DataFrame

To demonstrate how to display DataFrames of floats using a format string for columns, we need to create a DataFrame first. We can use the `pd.DataFrame` function to create a DataFrame with random float data.

``` python
df = pd.DataFrame(np.random.randn(5, 5), columns=['col1', 'col2', 'col3', 'col4', 'col5'])
print(df)
```

Output:

``` python
       col1      col2      col3      col4      col5
0 -0.002245  0.104297 -0.565902  0.160842  1.135332
1 -0.857941 -0.506034 -0.385378 -0.148127 -0.011758
2  0.710614  1.250324  0.137906 -0.196947 -0.748276
3 -0.115694 -0.748427 -1.670615 -0.404639 -0.477310
4  0.518831 -0.261777  0.720524  0.212153  0.704119
```

## Displaying Floats in a DataFrame with Format String

Now, to display floats with a format string, we can use the `pd.options.display.float_format` function. We can specify the format in the string using the curly braces and the `.format()` function. Here's an example:

``` python
pd.options.display.float_format = '{:,.2f}'.format
print(df)
```

Output:

``` python
   col1  col2  col3  col4  col5
0 -0.00  0.10 -0.57  0.16  1.14
1 -0.86 -0.51 -0.39 -0.15 -0.01
2  0.71  1.25  0.14 -0.20 -0.75
3 -0.12 -0.75 -1.67 -0.40 -0.48
4  0.52 -0.26  0.72  0.21  0.70
```

In the above example, we have specified the format string as `'{:,.2f}'`. This means that we want to display the float numbers with two decimal places and with a comma separator for thousand separators. 

## Resetting the Float Format to Default

To reset the format string to its default value, we can use the `pd.reset_option('display.float_format')` function. Here's an example:

``` python
pd.reset_option('display.float_format')
print(df)
```

Output:

``` python
       col1      col2      col3      col4      col5
0 -0.002245  0.104297 -0.565902  0.160842  1.135332
1 -0.857941 -0.506034 -0.385378 -0.148127 -0.011758
2  0.710614  1.250324  0.137906 -0.196947 -0.748276
3 -0.115694 -0.748427 -1.670615 -0.404639 -0.477310
4  0.518831 -0.261777  0.720524  0.212153  0.704119
```

In the above example, we have used the `pd.reset_option('display.float_format')` function to reset the format string to its default value.

# Conclusion

That's it! We have learned how to display pandas DataFrame of floats using a format string for columns in Python. If you have any questions, feel free to ask in the comments section.
