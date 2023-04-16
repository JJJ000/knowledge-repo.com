---
title: What is the quickest way to iterate over a dataframe using pandas?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: The most efficient way to loop through dataframes with pandas in Python is to use the iterrows() or itertuples() methods.
---

**Contents**

[TOC]

**Using Iterrows:**

1. Create an empty list to store the data.
2. Use the `iterrows()` method to iterate through each row of the DataFrame.
3. Append the row data to the empty list.
4. Return the list when all rows have been iterated.

**Using itertuples:**

1. Create an empty list to store the data.
2. Use the `itertuples()` method to iterate through each row of the DataFrame.
3. Append the row data to the empty list.
4. Return the list when all rows have been iterated.

**Using apply:**

1. Define a function to process each row of the DataFrame.
2. Use the `apply()` method to apply the function to each row of the DataFrame.
3. Return the processed DataFrame when all rows have been processed.

**Using Numpy Vectorization:**

1. Use the `np.vectorize()` method to vectorize the operations on the DataFrame.
2. Use the `np.apply_along_axis()` method to apply the vectorized operations to each row of the DataFrame.
3. Return the processed DataFrame when all rows have been processed.
