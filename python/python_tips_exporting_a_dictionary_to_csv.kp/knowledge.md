---
title: What is the method for saving a Python dictionary to a csv file?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-12 00:00:00
updated_at: 2023-03-12 00:00:00
tldr: Use the csv module in Python and use the writerow function to write each key-value pair in the dictionary as a row in the csv file.
---

**Contents**

[TOC]

## Section 1: Introduction

In this section, provide a brief overview of the purpose of the tutorial, which is to show how to write a Python dictionary to a CSV file.


## Section 2: Writing a dictionary to a CSV file

To write a dictionary to a CSV file in Python, you can use the csv module in Python. This module provides functionality to read from and write to CSV files. To write a dictionary to a CSV file, follow the steps below:

1. Import the csv module.

```python
import csv
```

2. Create a Python dictionary that will be written to the CSV file.

```python
data = {
    'Name': ['Alice', 'Bob', 'Charlie'],
    'Age': [25, 30, 35],
    'City': ['New York', 'London', 'Paris']
}
```

3. Open a CSV file in write mode using the `open()` function.

```python
with open('data.csv', 'w', newline='') as csvfile:
```

Note that we pass `newline=''` to ensure that newlines are not doubled.

4. Create a CSV writer object using the writer() method of the csv module.

```python
    writer = csv.writer(csvfile)
```

5. Write the header row to the CSV file using the writerow() method.

```python
    writer.writerow(['Name', 'Age', 'City'])
```

6. Write each row of data to the CSV file using the writerows() method.

```python
    for i in range(len(data['Name'])):
        writer.writerow([data['Name'][i], data['Age'][i], data['City'][i]])
```

7. Close the CSV file.

```python
csvfile.close()
```


## Section 3: Full code

Here is the full code to write a Python dictionary to a CSV file:

```python
import csv

data = {
    'Name': ['Alice', 'Bob', 'Charlie'],
    'Age': [25, 30, 35],
    'City': ['New York', 'London', 'Paris']
}

with open('data.csv', 'w', newline='') as csvfile:
    writer = csv.writer(csvfile)
    writer.writerow(['Name', 'Age', 'City'])
    for i in range(len(data['Name'])):
        writer.writerow([data['Name'][i], data['Age'][i], data['City'][i]])
csvfile.close()
```

This code will create a CSV file called 'data.csv' with the following contents:

```
Name,Age,City
Alice,25,New York
Bob,30,London
Charlie,35,Paris
```
