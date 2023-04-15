---
title: How can a csv string in Python be converted into an array?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-16 00:00:00
updated_at: 2023-04-16 00:00:00
tldr: Use Python`s built-in csv module and the csv.reader method to read the CSV string into a 2D array.
---

**Contents**

[TOC]

## Section 1: Introduction
The Comma Separated Values (CSV) file format is a popular way to store and retrieve data in a tabular format. The data in a CSV file is often represented as a string, with each line separated by a new line character and each value separated by a comma. In this tutorial, we will discuss how to convert a CSV string to an array in Python.

## Section 2: Using the csv module
Python's built-in csv module provides a convenient way to parse CSV files. We can use the csv.reader() function to iterate over the CSV string and convert it to a list of lists representing the rows and columns of the CSV file.

```python
importcsv

csv_string = "1,a,b\n2,c,d\n3,e,f"
rows = csv.reader(csv_string.splitlines()) # splitlines converts the string to a list of strings
csv_list = list(rows) # convert the iterator to a list
print(csv_list)
# Output: [['1', 'a', 'b'], ['2', 'c', 'd'], ['3', 'e', 'f']]
```

Here, we split the CSV string into a list of strings using the splitlines() function and pass it to the csv.reader() function. We then convert the iterator that the function returns to a list using the list() function.

## Section 3: Using the split() function
If you don't want to use the csv module, you can split the CSV string using the split() function. We can split each line using the new line character (\n) and split each value in a line using the comma (,).

```python
csv_string = "1,a,b\n2,c,d\n3,e,f"
csv_list = []
for line in csv_string.split("\n"):
    csv_list.append(line.split(","))
print(csv_list)
# Output: [['1', 'a', 'b'], ['2', 'c', 'd'], ['3', 'e', 'f']]
```

Here, we split the CSV string into a list of lines using the split() function and iterate over each line using a for loop. We split each line using the split() function again, this time using the comma (,) as a separator.

## Section 4: Conclusion
In this tutorial, we discussed how to convert a CSV string to an array in Python. We saw two ways to accomplish this: using the csv module and using the split() function. Understanding these methods will allow you to manipulate CSV data in your Python code with ease.
