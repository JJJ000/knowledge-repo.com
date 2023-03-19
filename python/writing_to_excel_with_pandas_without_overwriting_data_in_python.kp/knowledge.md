---
title: What is the method to write to an already-existing excel file without deleting data (using pandas)?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-12 00:00:00
updated_at: 2023-03-12 00:00:00
tldr: Create a pandas DataFrame from the new data and append it to the existing Excel sheet using the `mode=`a`` parameter of the `to\_excel()` method.
---

**Contents**

[TOC]

## Section 1: Introduction
Pandas is a versatile library in Python for managing data. It's especially useful for managing data in tabular formats such as CSV and Excel files. In this tutorial, we will show you how to write to an existing Excel file without overwriting the data.

## Section 2: Installing the Required Libraries
Before we can start, we will need to ensure we have pandas installed on our machine. If you haven’t installed it before, you can install it using pip.

```
pip install pandas
```

## Section 3: Writing to an Existing Excel File
In this section, we will demonstrate how to write to an existing Excel file, without overwriting old data. Here's the process:

### 3.1. Load Existing Excel File into Pandas DataFrame

Firstly, we will need to import the existing Excel file into a pandas DataFrame using the read_excel() function.

``` python
import pandas as pd

excel_file = pd.read_excel('path/to/excel_file.xlsx')
```

### 3.2. Append New Data to Existing Excel File

Next, we can append new data to this DataFrame using the append() method. When using this method, we will set the ignore_index parameter to True to ensure that the new data is appended without overwriting any existing data in the file.

``` python
new_data = {'First Name': ['John', 'Mike', 'Jessica'], 'Last Name': ['Doe', 'Smith', 'Jones'], 'Age': [28, 32, 19]}
excel_file_data = excel_file.append(pd.DataFrame(new_data), ignore_index=True)

print(excel_file_data)
```

### 3.3. Write Data Back to Excel File

Finally, we will use the to_excel() function to write the updated DataFrame back to the Excel file, without overwriting the existing data. 

``` python
excel_file_data.to_excel('path/to/excel_file.xlsx', index=False)
```
By adding `index=False`, the index of the DataFrame will not be included in the resulting Excel file.

## Section 4: Conclusion
By following the process described above, we can write new data to an existing excel file without overwriting the data that was already present in the file.
