---
title: Transforming a collection of lists in Python into a comma-separated values file
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: Use the csv module and its writerows() function to write a Python list of lists to a csv file.
---

**Contents**

[TOC]

# Introduction

Saving data in a CSV format is a common practice in data science when working with tabular data. In Python, converting a list of lists to a CSV file requires the use of the CSV module. In this article, we will learn how to write a Python list of lists to a CSV file using the CSV module.

# Creating a list of lists

To write a list of lists to a CSV file, we first need to create a list of lists in Python. Let's create a sample list of lists to demonstrate this.

```
data = [['Name', 'Age', 'Gender'],
        ['John', 25, 'Male'],
        ['Sara', 31, 'Female'],
        ['David', 22, 'Male']]
```

Here, we have created a list of lists containing information about people, including their name, age, and gender.

# Writing to a csv file

To write this list of lists to a CSV file, we will use the CSV module in Python. The CSV module provides functionality to read from and write to CSV files.

Here's how we can write our list of lists to a CSV file:

```
import csv

with open('data.csv', 'w', newline='') as file:
    writer = csv.writer(file)
    writer.writerows(data)
```

In the first line, we import the CSV module into our script. In the next line, we create a `with` statement to open a new CSV file in write mode. The `newline=''` parameter is necessary to prevent blank lines from being added between rows in the output file.

Inside the `with` statement, we create a CSV writer object using the `csv.writer()` class. We pass the `file` object and our list of lists `data` as arguments to the `writer.writerows()` method.

This will write the contents of our `data` list of lists to a new CSV file called 'data.csv'.

# Conclusion

In this article, we learned how to write a Python list of lists to a CSV file using the CSV module. We first created a sample list of lists containing information about people, and then we used the CSV module to write this list of lists to a new CSV file. This approach can be used for other list of lists as well.
