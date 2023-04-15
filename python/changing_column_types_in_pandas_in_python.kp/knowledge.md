---
title: Convert the data type of a column in a pandas dataframe
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Use the .astype() method to change the column type in a pandas DataFrame.
---

**Contents**

[TOC]

**1. Using astype() Method**

The astype() method is used to explicitly convert one data type to another. We can pass any Python, Numpy or Pandas datatype to change all columns of a dataframe to that type, or we can pass a dictionary having column names as keys and data type as values to change the type of selected columns.

Syntax:

Dataframe.astype(dtype, copy=True, errors=’raise’)

Parameters:

dtype: Data type to which we want to convert.

copy: If true, a new object is created.

errors: Control raising of exceptions on invalid data for provided data type.

**2. Using to_numeric() Method**

The to_numeric() method is used to convert a column of a DataFrame or a Series to numeric values. It can also be used to convert strings to numbers.

Syntax:

pandas.to_numeric(arg, errors=’raise’, downcast=None)

Parameters:

arg: A scalar, list, tuple, 1-d array, or Series.

errors: If ‘raise’, then invalid parsing will raise an exception.

downcast: Downcasting is a process of changing the data type of a column to a lower form.

**3. Using astype() and to_numeric() Together**

We can also use both astype() and to_numeric() methods together to convert a column of a DataFrame to numeric values.

Syntax:

Dataframe.astype({‘column_name’: ‘float’}). to_numeric(errors=’coerce’)

Parameters:

column_name: Name of the column to be converted.

errors: If ‘coerce’, then invalid parsing will be set as NaN.

**4. Using apply() Method**

The apply() method is used to apply a function along an axis of the DataFrame. It can be used to convert a column of a DataFrame to numeric values.

Syntax:

Dataframe.apply(pd.to_numeric, errors=’coerce’, axis=0)

Parameters:

errors: If ‘coerce’, then invalid parsing will be set as NaN.

axis: Axis along which the function is applied.
