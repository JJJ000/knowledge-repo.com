---
title: What is the standard way to format a date when printing?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Use the datetime.strftime() method to print a date in a regular format in Python.
---

**Contents**

[TOC]

#Using the datetime Library

##Step 1: Import the datetime Library

In order to print a date in a regular format, we need to use the datetime library. To do this, we need to import the library at the beginning of our code. 

```python
import datetime
```

##Step 2: Create a datetime Object

Once we have imported the library, we can create a datetime object. This is done by passing a year, month, and day to the datetime constructor. 

```python
date = datetime.datetime(2020, 4, 15)
```

##Step 3: Format the Date

We can use the `strftime()` method to format the date. This method takes a string as an argument, which specifies the format of the date. 

```python
formatted_date = date.strftime("%m/%d/%Y")
```

##Step 4: Print the Formatted Date

Finally, we can print the formatted date using the `print()` function. 

```python
print(formatted_date)
```

The output of this code will be: `04/15/2020`
