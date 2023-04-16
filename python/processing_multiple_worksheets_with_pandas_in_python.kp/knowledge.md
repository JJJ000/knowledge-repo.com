---
title: Using pandas to read in multiple worksheets from the same excel workbook via pd.read_excel()
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Pandas can read multiple worksheets from the same workbook using the pd.read\_excel() function by specifying the sheet\_name parameter as a list of strings.
---

**Contents**

[TOC]

**Section 1: Overview**

Pandas is a powerful library in Python for data analysis and manipulation. It offers a wide range of functions for reading, writing, and manipulating data stored in various formats, including Excel. One of the most useful functions for working with Excel data is the pd.read_excel() function, which can be used to read multiple worksheets of the same workbook. This tutorial will explain how to use this function to read multiple worksheets of the same workbook in Python.

**Section 2: Importing the Library and Data**

To begin, we need to import the Pandas library and the Excel workbook we want to read. We can do this by using the following code:

```
import pandas as pd

workbook = pd.ExcelFile('example.xlsx')
```

**Section 3: Reading the Data**

Once the workbook is imported, we can use the pd.read_excel() function to read the data from each worksheet. The syntax for this function is as follows:

```
df = pd.read_excel(workbook, sheet_name='sheet_name')
```

Where `workbook` is the Excel file we imported earlier, and `sheet_name` is the name of the worksheet we want to read. We can use a loop to read each worksheet in the workbook, like this:

```
sheets = workbook.sheet_names

for sheet in sheets:
    df = pd.read_excel(workbook, sheet_name=sheet)
```

**Section 4: Storing the Data**

Once the data is read, we can store it in a list or dictionary. For example, we can store the data in a dictionary like this:

```
data = {}

for sheet in sheets:
    df = pd.read_excel(workbook, sheet_name=sheet)
    data[sheet] = df
```

Now the data from each worksheet is stored in the `data` dictionary, with the worksheet name as the key.
