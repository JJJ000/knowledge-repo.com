---
title: Adding an extra carriage return to a csv file in Python on windows
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Use the `\r\n` escape sequence when writing to the CSV file.
---

**Contents**

[TOC]

### Using the csv Module

The [csv module](https://docs.python.org/3/library/csv.html) in Python provides a number of methods for manipulating CSV files. To add an extra carriage return to a CSV file, you can use the `writerow()` method.

```python
import csv

# Open the CSV file
with open('myfile.csv', 'w', newline='') as csvfile:
    writer = csv.writer(csvfile)

# Write the data
writer.writerow(['column1', 'column2', 'column3'])
writer.writerow(['data1', 'data2', 'data3'])

# Add an extra carriage return
writer.writerow([])

# Write more data
writer.writerow(['column1', 'column2', 'column3'])
writer.writerow(['data4', 'data5', 'data6'])
```

### Using the sys Module

The [sys module](https://docs.python.org/3/library/sys.html) in Python provides access to system-specific parameters and functions. To add an extra carriage return to a CSV file, you can use the `stdout.write()` method.

```python
import sys

# Open the CSV file
with open('myfile.csv', 'w', newline='') as csvfile:

# Write the data
writer.writerow(['column1', 'column2', 'column3'])
writer.writerow(['data1', 'data2', 'data3'])

# Add an extra carriage return
sys.stdout.write('\r\n')

# Write more data
writer.writerow(['column1', 'column2', 'column3'])
writer.writerow(['data4', 'data5', 'data6'])
```

### Using the os Module

The [os module](https://docs.python.org/3/library/os.html) in Python provides a portable way of using operating system dependent functionality. To add an extra carriage return to a CSV file, you can use the `write()` method.

```python
import os

# Open the CSV file
with open('myfile.csv', 'w', newline='') as csvfile:

# Write the data
writer.writerow(['column1', 'column2', 'column3'])
writer.writerow(['data1', 'data2', 'data3'])

# Add an extra carriage return
os.write(csvfile.fileno(), '\r\n'.encode())

# Write more data
writer.writerow(['column1', 'column2', 'column3'])
writer.writerow(['data4', 'data5', 'data6'])
```
