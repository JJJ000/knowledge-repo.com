---
title: Can pandas.excelwriter be used to automatically adjust the column widths in excel?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-18 00:00:00
updated_at: 2023-04-18 00:00:00
tldr: Yes, by setting the `auto\_fit` parameter to `True` in the `to\_excel()` method when using `pandas.ExcelWriter`.
---

**Contents**

[TOC]

Section 1: Introduction
-----------------------
When working with large datasets in Excel, it is often necessary to manually adjust the column widths to ensure that data is displayed properly. This can be a time-consuming process, especially when dealing with hundreds or thousands of rows. The pandas.ExcelWriter module in Python provides a convenient way to write data to an Excel file, but it does not offer an automatic way to adjust column widths.

Section 2: The Problem
----------------------
The issue of adjusting column widths arises when dealing with data that has varying lengths, such as strings or dates. If the column width is too narrow, the data may be truncated and difficult to read. If the column width is too wide, it may take up unnecessary space and make it harder to navigate the spreadsheet.

Section 3: The Solution
-----------------------
While pandas.ExcelWriter does not have a built-in method to automatically adjust column widths, there is a workaround that involves using the xlsxwriter module. This module allows you to format the Excel file after it has been written by pandas to disk. Using xlsxwriter, you can set the column widths based on the length of the data in each column.

The following code demonstrates how to create an Excel writer, set the column widths based on the length of the values, and write the data to the file:

```
import pandas as pd
import xlsxwriter

# Create a dataframe
df = pd.DataFrame({
    'column1': ['This is a very long string', 'Short', 'Medium'],
    'column2': [123456789, 12, 123456],
    'column3': ['2022-01-01', '2022-02-01', '2022-03-01']
})

# Create a Pandas Excel writer using XlsxWriter as the engine.
writer = pd.ExcelWriter('example.xlsx', engine='xlsxwriter')

# Write the DataFrame to a sheet in the Excel file.
df.to_excel(writer, sheet_name='Sheet1', index=False)

# Get the xlsxwriter workbook and worksheet objects.
workbook  = writer.book
worksheet = writer.sheets['Sheet1']

# Set the column widths based on the length of values in each cell.
for i, col in enumerate(df.columns):
    column_len = max(df[col].astype(str).map(len).max(), len(col))
    worksheet.set_column(i, i, column_len + 1)

# Close the Pandas Excel writer and output the Excel file.
writer.save()
```

In this example, the code first creates a simple dataframe with columns of different lengths. It then creates an Excel writer using xlsxwriter as the engine, writes the data to a sheet in the Excel file, gets the xlsxwriter workbook and worksheet objects, and loops through each column in the dataframe to set the column width based on the length of the values.

Section 4: Conclusion
----------------------
While the pandas.ExcelWriter module does not have a built-in way to automatically adjust column widths, the xlsxwriter module provides a workaround that allows you to format the Excel file after it has been written to disk. By setting the column widths based on the length of the data in each column, you can ensure that the data is displayed in a clear and organized manner, without having to manually adjust the column widths.
