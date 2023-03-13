---
title: What is the process of adding a new sheet to an already existing excel file utilizing pandas?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-13 00:00:00
updated_at: 2023-03-13 00:00:00
tldr: Use the `to\_excel()` function with the parameter `sheet\_name` set to the desired sheet name and `mode` set to ``a`` to append the sheet to the existing Excel file.
---

**Contents**

[TOC]

## Section 1: Introduction
Pandas is a popular open-source data manipulation library for Python. It is widely used for data analysis, data visualization, and data cleaning tasks. In this tutorial, we will learn how to save a new sheet in an existing Excel file using Pandas in Python.

## Section 2: Reading the Excel file
Before we can add a new sheet to an existing Excel file, we first need to read the file into a Pandas DataFrame. We can use the `read_excel()` function in Pandas to do this. The `read_excel()` function takes the path of the Excel file as its argument and returns a DataFrame.

```python
import pandas as pd

excel_file = pd.read_excel('file_path.xlsx')
```

## Section 3: Saving a new sheet in the Excel file
To add a new sheet in an existing Excel file, we can use the `ExcelWriter()` object in Pandas. The `ExcelWriter()` object provides a `sheet_name` parameter that we can use to specify the name of the new sheet.

```python
writer = pd.ExcelWriter('file_path.xlsx', engine='openpyxl')
excel_file.to_excel(writer, sheet_name='new_sheet')
writer.save()
```

In the code above, we first create an `ExcelWriter()` object and pass the path of the Excel file as its argument. We also specify the engine as `openpyxl` since it is the recommended engine for working with Excel files. Next, we use the `to_excel()` function on the DataFrame object and pass the `writer` object and the name of the new sheet as arguments. Finally, we save the changes to the Excel file using the `save()` function on the `writer` object.

## Section 4: Conclusion
In this tutorial, we learned how to save a new sheet in an existing Excel file using Pandas in Python. We first read the Excel file into a Pandas DataFrame using the `read_excel()` function, and then used the `ExcelWriter()` object to add a new sheet to the Excel file. We hope this tutorial was helpful.
