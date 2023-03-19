---
title: Searching for the sheet names within an excel file using pandas
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: Use the pandas.ExcelFile.sheet\_names command to get the list of sheets in an excel file in Python using pandas.
---

**Contents**

[TOC]

Section 1: Introduction
In Python, we can use the Pandas library to read and manipulate data from Excel files. When reading an Excel file, in addition to specifying the file path and name, we need to specify the sheet name if we want to read or manipulate data from a particular sheet. Sometimes, we may have an Excel file with multiple sheets and we need to know the sheet names to be able to work efficiently. In this case, we can use Pandas to look up the list of sheets in the Excel file.

Section 2: Code to look up the list of sheets
To look up the list of sheets in an Excel file using Pandas, we need to first import the Pandas library and read the Excel file using the pd.ExcelFile() method. Then, we can use the sheet_names attribute of the ExcelFile object to get the list of sheet names.

Here's the code:

```python
import pandas as pd

# specify the file path and name
file_path = 'example.xlsx'

# create the ExcelFile object
excel_file = pd.ExcelFile(file_path)

# get the list of sheet names
sheet_names = excel_file.sheet_names

print(sheet_names)
```

This code will output a list of sheet names in the Excel file.

Section 3: Example output
Here's an example of what the output may look like:

```python
['Sheet1', 'Sheet2', 'Sheet3']
```

This means that the Excel file we're working with has three sheets named Sheet1, Sheet2, and Sheet3.

Section 4: Conclusion
Using Pandas, we can easily look up the list of sheets in an Excel file. This can be helpful when working with large Excel files with multiple sheets. By knowing the sheet names, we can efficiently extract and manipulate data from specific sheets without having to manually look up the sheet names every time.
