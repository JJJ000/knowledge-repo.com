---
title: How to generate a dictionary using a csv file?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-07 00:00:00
updated_at: 2023-03-07 00:00:00
tldr: Use the `csv` module and iterate through each row to add key-value pairs to a Python dictionary.
---

**Contents**

[TOC]

## Reading in the CSV file

The first step in creating a dictionary from a csv file in Python is to read in the csv file using the csv module. We will open the file using the built-in `open()` function, and then create a csv reader object using the `csv.reader()` function.

```python
import csv

with open('data.csv', 'r') as file:
    reader = csv.reader(file)
    for row in reader:
        print(row)
```

This code will open a file called `data.csv` and read its contents, printing each row to the console. 

## Converting the CSV to a Dictionary

To convert the CSV to a dictionary, we will use the csv reader to loop through each row in the file and create a dictionary where the keys are the column headers and the values are the corresponding row values.

```python
import csv

with open('data.csv', 'r') as file:
    reader = csv.reader(file)
    header = next(reader)
    data = []
    for row in reader:
        temp_dict = {}
        for i in range(len(header)):
            temp_dict[header[i]] = row[i]
        data.append(temp_dict)
```

In this code, we first get the header row using the `next()` function on the reader object. We then loop through each row in the reader object and create a temporary dictionary with the header keys and row values. We then append this dictionary to a list called `data` which will eventually hold all of the dictionaries.

## Using the Dictionary

Once we have created the dictionary from the CSV file, we can use it just like any other Python dictionary.

```python
print(data[0]['Name'])
```

This code would print the value of the 'Name' key in the first dictionary in the `data` list. 

We can also loop through the `data` list and perform operations on each dictionary.

```python
for entry in data:
    print(entry['Name'], ':', entry['Age'])
```

This code would print out each name and age in the `data` list, separated by a colon.
