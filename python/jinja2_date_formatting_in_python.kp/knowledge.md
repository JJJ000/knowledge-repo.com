---
title: What is the process for formatting a date in jinja2?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: Use the built-in strftime filter with the desired format.
---

**Contents**

[TOC]

## Introduction

In Jinja2, formatting a date is a common task. Luckily, it is quite easy to do. This guide shows how to format a date in Jinja2 in Python in simple steps.

## Step 1: Import datetime

Before we can format a date in Jinja2, we must import the `datetime` module in Python. This module is used for working with dates and times.

```python
from datetime import datetime
```

## Step 2: Create a date object

To format a date in Jinja2, we must first create a date object. We can create a date object using the `datetime` module's `strptime()` function.

```python
date_object = datetime.strptime('2022-10-12', '%Y-%m-%d')
```

In this example, we are creating a new date object for October 12, 2022.

## Step 3: Format the date object

Once we have created a date object, we can format it using the `strftime()` method. This method takes a format string as its argument and returns a string representation of the date in the desired format.

```python
formatted_date = date_object.strftime('%B %d, %Y')
```

In this example, we are formatting the date object to display the month name, day, and year, separated by commas.

## Step 4: Pass the formatted date to Jinja2

The final step is to pass the formatted date to Jinja2. We can do this by passing the `formatted_date` variable to the template as a context variable.

```python
from flask import Flask, render_template

app = Flask(__name__)

@app.route('/')
def index():
    date_object = datetime.strptime('2022-10-12', '%Y-%m-%d')
    formatted_date = date_object.strftime('%B %d, %Y')
    return render_template('index.html', date=formatted_date)
```

In this example, we are passing the `formatted_date` variable to the `index.html` template as a context variable named `date`.

## Conclusion

That's it! We have successfully formatted a date in Jinja2 in Python. By following the above steps, we can easily format dates in Jinja2 according to our needs.
