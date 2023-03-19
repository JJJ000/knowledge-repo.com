---
title: What is the process of transforming this collection of dictionaries into a csv file?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: Use the csv module`s DictWriter function to write each dictionary to a row in the csv file.
---

**Contents**

[TOC]

## Section 1: Loading Data
First, you need to load the data into Python by creating a list of dictionaries.

```
data = [{'name': 'John Smith', 'age': 25, 'city': 'New York'},
        {'name': 'Jane Doe', 'age': 30, 'city': 'Los Angeles'},
        {'name': 'Bob Johnson', 'age': 50, 'city': 'Chicago'}]
```

## Section 2: Writing to CSV
Next, you can use the `csv` module to write the data into a CSV file.

```
import csv

with open('data.csv', 'w', newline='') as file:
    writer = csv.writer(file)
    # Write headers to CSV
    writer.writerow(data[0].keys())
    # Write data to CSV
    for row in data:
        writer.writerow(row.values())
```

The `csv.writer()` function takes a file object and returns a writer object that allows you to write data to the file. The `writerow()` function is used to write a single row of data to the CSV file.

In the `with` block, we first write the headers to the CSV file by using the `keys()` method of the first dictionary in the list. Then we loop through each dictionary in the list and write the values to the CSV file using the `values()` method.

## Section 3 (Optional): Reading from CSV
You may also want to know how to read data from the CSV file you just created. Here's how you can do it:

```
import csv

with open('data.csv', 'r') as file:
    reader = csv.reader(file)
    # Skip headers
    next(reader)
    # Read data
    for row in reader:
        print(row)
```

The `csv.reader()` function takes a file object and returns a reader object that allows you to read data from the file. The `next()` function is used to skip the first row, which is assumed to be the header row. Then we loop through each row in the CSV file and print it to the console. The `row` variable is a list of values from the CSV file. 

## Section 4: Additional Notes
When working with CSV files, keep in mind that they do not inherently store data types like lists and dictionaries do. All values in a CSV file are stored as strings. If you want to work with other data types, you will need to convert them after reading the data from the CSV file or before writing the data to the CSV file.
