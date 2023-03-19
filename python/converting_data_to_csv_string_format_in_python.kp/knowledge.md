---
title: Can you guide me on converting data into a string formatted as csv, without saving it as a file?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-12 00:00:00
updated_at: 2023-03-12 00:00:00
tldr: You can use the StringIO class from the io module to write CSV data as a string in Python.
---

**Contents**

[TOC]

## Section 1: Introduction
CSV (Comma Separated Values) is a popular file format used to store tabular data in plain text. Python provides a built-in module called `csv` to read and write data in CSV format. In this tutorial, we will learn how to write data into CSV format as a string in Python.

## Section 2: Writing Data into CSV String

To write data into a CSV string in Python, we need to follow these steps:

1. import the `csv` module
2. create a string buffer using StringIO module
3. create a CSV writer object using `csv.writer` method
4. write data into the CSV writer object
5. get the CSV string from the string buffer using `getvalue` method


Here's the code for the above steps:
```python
import csv
from io import StringIO

# create a string buffer using StringIO module
csv_str_buffer = StringIO()

# create a CSV writer object
csv_writer = csv.writer(csv_str_buffer)

# write data into the CSV writer object
csv_writer.writerow(['Name', 'Age', 'Country'])
csv_writer.writerow(['John', '25', 'USA'])
csv_writer.writerow(['Mary', '30', 'UK'])

# get the CSV string
csv_string = csv_str_buffer.getvalue()

print(csv_string)
```

Output:
```
Name,Age,Country\r\n
John,25,USA\r\n
Mary,30,UK\r\n
```

## Section 3: Writing Data with Different Delimiters and Line Endings

By default, Python's CSV module uses commas as delimiters and `\r\n` as line endings. However, we can change these values as per our requirements.

Here's an example where we write data with semicolon as delimiter and `\n` as line ending:
```python
import csv
from io import StringIO

# create a string buffer using StringIO module
csv_str_buffer = StringIO()

# create a CSV writer object with semicolon as delimiter and \n as line ending
csv_writer = csv.writer(csv_str_buffer, delimiter=';', lineterminator='\n')

# write data into the CSV writer object
csv_writer.writerow(['Name', 'Age', 'Country'])
csv_writer.writerow(['John', '25', 'USA'])
csv_writer.writerow(['Mary', '30', 'UK'])

# get the CSV string
csv_string = csv_str_buffer.getvalue()

print(csv_string)
```
Output:
```
Name;Age;Country\n
John;25;USA\n
Mary;30;UK\n
```

## Section 4: Conclusion
In this tutorial, we have learned how to write data into a CSV format as a string in Python. We also learned how to change the delimiter and line ending characters in the CSV output. With this knowledge, we can easily write data into a string buffer, which we can then use for various purposes such as sending over HTTP requests, saving in databases, writing in files, etc.
