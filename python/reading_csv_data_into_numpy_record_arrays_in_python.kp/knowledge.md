---
title: What is the process for importing csv data into a record array using numpy?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-01 00:00:00
updated_at: 2023-02-01 00:00:00
tldr: Use the numpy.genfromtxt() function to read CSV data into a record array in NumPy.
---

**Contents**

[TOC]

#Reading a CSV File
1. Import the NumPy module: 
```python
import numpy as np
```
2. Load the CSV file into a NumPy record array: 
```python
data = np.recfromcsv('filename.csv')
```

#Accessing Data
1. Accessing data from the record array: 
```python
data['column_name']
```
2. Accessing specific elements from the record array: 
```python
data[index]['column_name']
```
