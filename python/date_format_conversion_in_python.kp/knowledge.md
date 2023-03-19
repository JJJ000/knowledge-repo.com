---
title: Reformat date string from its current format
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-07 00:00:00
updated_at: 2023-03-07 00:00:00
tldr: Use the datetime module to parse the date string and then use strftime() method to change format.
---

**Contents**

[TOC]

## Section 1: Introduction
In Python, the `datetime` module provides classes for working with dates and times. It includes a `datetime.strptime()` method which can parse a string representation of a date and time into a `datetime` object. Once we have the `datetime` object, we can format it into any desired date format using the `strftime()` method. In this tutorial, we will learn how to parse a date string and change its format.

## Section 2: Parsing a date string
To parse a date string, we can use the `datetime.strptime()` method. This method takes two arguments: the first argument is the date string to be parsed, and the second argument is the format string that specifies the format of the date string. The format string consists of various format codes that represent different parts of the date and time.

Here's an example code that parses a date string into a `datetime` object:

```python
from datetime import datetime

date_string = "2022-01-05 12:30:45"
format_string = "%Y-%m-%d %H:%M:%S"

datetime_object = datetime.strptime(date_string, format_string)
print(datetime_object)
```

Output:
```
2022-01-05 12:30:45
```

In the above code, we have a date string `2022-01-05 12:30:45` and a format string `%Y-%m-%d %H:%M:%S`. The format string specifies that the year should be represented by 4 digits (`%Y`), the month by 2 digits (`%m`), the day by 2 digits (`%d`), the hour by 24-hour format (`%H`), the minute by 2 digits (`%M`), and the second by 2 digits (`%S`). The `datetime.strptime()` method returns a `datetime` object that represents the parsed date and time.

## Section 3: Changing the date format
Once we have the `datetime` object, we can format it into any desired date format using the `strftime()` method. The `strftime()` method takes a format string as an argument that specifies the desired output format.

Here's an example code that changes the format of a `datetime` object:

```python
from datetime import datetime

date_string = "2022-01-05 12:30:45"
format_string = "%Y-%m-%d %H:%M:%S"

datetime_object = datetime.strptime(date_string, format_string)

new_format_string = "%d %B %Y %I:%M %p"   # day month year hour:min AM/PM
formatted_date = datetime_object.strftime(new_format_string)

print(formatted_date)
```

Output:
```
05 January 2022 12:30 PM
```

In the above code, we have used the `strftime()` method to format the `datetime` object into a new format. We have used `%d` for the day, `%B` for the full month name, `%Y` for the year with century, `%I` for the hour in 12-hour format, `%M` for the minute, and `%p` for the AM/PM designation.

## Section 4: Conclusion
In this tutorial, we have learned how to parse a date string and change its format in Python. We have used the `datetime.strptime()` method to parse the date string into a `datetime` object, and the `strftime()` method to change its format. The `datetime` module provides a powerful tool for working with dates and times in Python.
