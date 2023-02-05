---
title: What is the name of the month corresponding to a given number?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: The month name corresponding to a given number can be obtained using the datetime module`s month\_name function.
---

**Contents**

[TOC]

# Section 1: Using Dictionary

We can use a dictionary to map the month numbers to their corresponding month names.

```python
month_dict = {
    1: "January",
    2: "February",
    3: "March",
    4: "April",
    5: "May",
    6: "June",
    7: "July",
    8: "August",
    9: "September",
    10: "October",
    11: "November",
    12: "December"
}

month_number = int(input("Enter month number: "))

month_name = month_dict[month_number]

print(month_name)
```

# Section 2: Using List

We can also use a list to store the month names and access them using the index.

```python
month_list = ["January", "February", "March", "April", "May", "June", "July", "August", "September", "October", "November", "December"]

month_number = int(input("Enter month number: "))

month_name = month_list[month_number-1]

print(month_name)
```

# Section 3: Using DateTime Module

We can also use the datetime module to get the month name from the month number.

```python
import datetime

month_number = int(input("Enter month number: "))

month_name = datetime.date(1900, month_number, 1).strftime('%B')

print(month_name)
```

# Section 4: Using Calendar Module

We can also use the calendar module to get the month name from the month number.

```python
import calendar

month_number = int(input("Enter month number: "))

month_name = calendar.month_name[month_number]

print(month_name)
```
