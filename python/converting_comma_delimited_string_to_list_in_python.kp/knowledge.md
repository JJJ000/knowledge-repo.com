---
title: In python, what is the procedure for converting a string containing items separated by commas into a list?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-18 00:00:00
updated_at: 2023-04-18 00:00:00
tldr: You can convert a string with comma-delimited items to a list in Python using the split() method.
---

**Contents**

[TOC]

## Converting a Comma-Delimited String to a List in Python

Python provides several ways to convert a comma-delimited string into a list. In this tutorial, we will explore three common approaches to accomplish this task.

### Method 1: Using the split() Function

The split() function is a built-in method in Python that can be used to split a string into a list of substrings based on the specified delimiter. To convert a comma-delimited string to a list, we can pass the string and the comma delimiter as arguments to the split() function.

```python
string = "apple, banana, cherry, date"
my_list = string.split(", ")
print(my_list)
```

Output:
```
['apple', 'banana', 'cherry', 'date']
```

### Method 2: Using the csv Module

Python also has a built-in csv module that is designed to handle csv files and string imports easily. To use this module on a string object with comma-separated values, we can pass the string object to the `csv.reader()` function.

```python
import csv
string = "apple, banana, cherry, date"
my_list = list(csv.reader([string]))
print(my_list[0])
```

Output:
```
['apple', ' banana', ' cherry', ' date']
```

### Method 3: Using the re Module

The re (regular expression) module can also be used to split a string into a list of substrings based on a delimiter. This method is useful when more complex delimiters are required and the `split()` approach does not suffice. For comma-separated values, we can pass the comma delimiter `','` to the regular expression `re.split()` function.

```python
import re
string = "apple, banana, cherry, date"
my_list = re.split(r'\s*,\s*', string)
print(my_list)
```

Output:
```
['apple', 'banana', 'cherry', 'date']
```
