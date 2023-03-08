---
title: What is the method to use Python to write data into an excel spreadsheet?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-08 00:00:00
updated_at: 2023-03-08 00:00:00
tldr: Use the Python package called `openpyxl` to write to an Excel spreadsheet.
---

**Contents**

[TOC]

## Introduction
Python provides several libraries that allow easy reading and writing data from/to an Excel spreadsheet. These libraries include `openpyxl`, `xlrd`, and `xlwt`. In this article, we will demonstrate how to write data to an Excel spreadsheet using `openpyxl` library.

## Installing openpyxl
Before we begin, we need to install the `openpyxl` library. The easiest way to install it is to use pip, a package installer for Python. To install openpyxl using pip, open your terminal window and type the following command:

```python
pip install openpyxl
```

## Creating a new Excel workbook
To create a new Excel workbook using openpyxl, we first need to import it as follows:

```python
import openpyxl
```

Next, we create a new workbook using the `Workbook()` method:

```python
workbook = openpyxl.Workbook()
```

Now that we have created a workbook, we can add a new worksheet using the `create_sheet()` method:

```python
worksheet = workbook.create_sheet("Sheet1")
```

Alternatively, we can add a new worksheet at a specific index as follows:

```python
worksheet = workbook.create_sheet("Sheet1", 0)
```
Here, the `0` indicates that we want to add the worksheet at index 0. 

## Writing to an Excel spreadsheet
Once we have created a worksheet, we can write data to it using the `cell()` method. The `cell()` method takes two arguments: the row index and the column index. To write a value to a cell, we simply assign it to the `value` attribute of the cell object. For instance, to write the value "Hello, World!" to cell A1, we do the following:

```python
worksheet.cell(row=1, column=1).value = "Hello, World!"
```

We can also write data to multiple cells at once using a loop. For instance, the following code writes the numbers 1 to 5 to the cells in column A starting at row 2:

```python
for i in range(1, 6):
    worksheet.cell(row=i+1, column=1).value = i
```

Finally, once we have finished writing data to the worksheet, we need to save the workbook using the `save()` method:

```python
workbook.save(filename="example.xlsx")
```

This will create a new Excel spreadsheet called `example.xlsx` in the current directory with the data we have written to it. 

## Conclusion
In this article, we have shown how to write data to an Excel spreadsheet using the openpyxl library. We first installed the library and then demonstrated how to create a new workbook and worksheet, and how to write data to it using the `cell()` method. Finally, we saved the workbook to the disk. With this knowledge, you should be able to create and write data to your own Excel spreadsheets using Python.
