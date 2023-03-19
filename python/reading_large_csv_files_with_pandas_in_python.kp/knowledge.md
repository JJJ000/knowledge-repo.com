---
title: What is the process to utilize pandas for reading a huge csv file?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-05 00:00:00
updated_at: 2023-03-05 00:00:00
tldr: Use the `pandas.read\_csv()` function with appropriate parameters, such as specifying the file path and delimiter, to read a large csv file in Python.
---

**Contents**

[TOC]

## Importing pandas library
- The first step in reading a large CSV file in pandas is to import the library. We will start by writing the following code:

``` python
import pandas as pd
```

## Using the read_csv() function
- Now that we have imported the pandas library, we can use the read_csv() function to read the CSV file. The read_csv() function in pandas reads a CSV file into DataFrame format. To use this function, we need to specify the path of the CSV file.

``` python
data = pd.read_csv('path_to_file.csv')
```

## Using chunksize in read_csv() function
- If the CSV file is very large and you don't have enough memory to load the complete file at once, you can use the 'chunksize' parameter in the read_csv() function. This parameter allows you to read the CSV file in smaller chunks.

``` python
data_chunks = pd.read_csv('path_to_file.csv', chunksize=1000)
for chunk in data_chunks:
    #perform any manipulation on the data
```

## Conclusion
- These are some of the ways you can read a large CSV file in pandas. You can use any of the above-mentioned methods depending on your needs and requirements. Once you have read the CSV file into a pandas DataFrame, you can perform any manipulation or analysis you want on the data.
