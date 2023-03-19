---
title: What is the most pythonic and clean approach to obtain the date of tomorrow?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-11 00:00:00
updated_at: 2023-03-11 00:00:00
tldr: The cleanest and most Pythonic way to get tomorrow`s date is by using the `date.today()` method from the `datetime` module and adding one day with the `.timedelta()` method. 

```python
from datetime import date, timedelta
tomorrow = date.today() + timedelta(days=1)
```
---

**Contents**

[TOC]

## Importing the datetime module
We first import the "datetime" module which provides a way to work with dates and times.

```python
import datetime
```

## Getting tomorrow's date
We can obtain tomorrow's date by adding one day to today's date. We use the `datetime.date.today()` method to get today's date and then add a day using the `datetime.timedelta` method.

```python
tomorrow = datetime.date.today() + datetime.timedelta(days=1)
```

## Outputting the date
We can then print tomorrow's date in a desired format by using the `strftime()` method. 

```python
print(tomorrow.strftime('%Y-%m-%d'))
```

This will output the date in the format "YYYY-MM-DD" which is often used in databases.

## Final code
```python
import datetime

tomorrow = datetime.date.today() + datetime.timedelta(days=1)

print(tomorrow.strftime('%Y-%m-%d'))
``` 

This is clean and effective code in getting tomorrow's date in a most pyhonic way.
