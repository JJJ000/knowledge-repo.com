---
title: What is the process to add a new row to an existing csv file using python?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-05 00:00:00
updated_at: 2023-03-05 00:00:00
tldr: Open the CSV file in append mode and pass the new row as a list to the writer object`s writerow() method.
---

**Contents**

[TOC]

## Introduction

CSV (Comma Separated Value) files are text files used to store tabular data. Python has a built-in module called `csv` for handling CSV files. In this tutorial, we will discuss how to append a new row to an old CSV file using Python.

## Appending a new row to a CSV file

To append a new row to a CSV file, follow these steps:

1. Open the CSV file in append mode using the `open()` function. Set the mode parameter to `'a'`, which stands for append. 

```python
with open('data.csv', mode='a', newline='') as file:
    writer = csv.writer(file)
```

2. Create a CSV writer object using the `writer()` function from the `csv` module. 

```python
with open('data.csv', mode='a', newline='') as file:
    writer = csv.writer(file)
```

3. Call the `writerow()` method on the writer object, passing in a list or tuple containing the data for the new row. 

```python
new_row = ['John', 'Doe', '42']
with open('data.csv', mode='a', newline='') as file:
    writer = csv.writer(file)
    writer.writerow(new_row)
```

4. Close the file using the `close()` method.

```python
with open('data.csv', mode='a', newline='') as file:
    writer = csv.writer(file)
    writer.writerow(new_row)
file.close()
```

## Complete example

Here is a complete example that reads a CSV file containing two rows of data, appends a new row to the file, and then reads and prints the updated data.

```python
import csv

# read original data
with open('data.csv', mode='r') as file:
    reader = csv.reader(file)
    for row in reader:
        print(row)

# append a new row
new_row = ['John', 'Doe', '42']
with open('data.csv', mode='a', newline='') as file:
    writer = csv.writer(file)
    writer.writerow(new_row)

# read updated data
with open('data.csv', mode='r') as file:
    reader = csv.reader(file)
    for row in reader:
        print(row)
```

This code will output:

```
['Alice', 'Smith', '25']
['Bob', 'Johnson', '30']
['Alice', 'Smith', '25']
['Bob', 'Johnson', '30']
['John', 'Doe', '42']
```

As you can see, the new row containing `'John', 'Doe', '42'` has been appended to the end of the file. 

## Conclusion

In this tutorial, we discussed how to append a new row to an old CSV file using Python. We covered the steps involved and provided a complete example. With this knowledge, you can easily manipulate and update CSV files using Python.
