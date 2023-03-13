---
title: Define the format of date for input arguments in Python argparse
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-13 00:00:00
updated_at: 2023-03-13 00:00:00
tldr: The date format for Python argparse input arguments should be specified using the `dateutil.parser.parse()` function.
---

**Contents**

[TOC]

There are different date formats that Python argparse can accept as input arguments. Here are four sections that describe the most common formats:

## ISO 8601 format
ISO 8601 is an international standard for representing date and time in a structured format. It has a syntax of YYYY-MM-DDTHH:MM:SS.mmmmmm, where:

- YYYY is the four-digit year
- MM is the two-digit month
- DD is the two-digit day of the month
- T separates the date and time
- HH is the two-digit hour (in 24-hour format)
- MM is the two-digit minute
- SS is the two-digit second
- .mmmmmm represents microseconds (optional)

To parse a date argument in ISO 8601 format using argparse, you can use the `dateutil.parser` module:

```python
import argparse
from dateutil.parser import parse

parser = argparse.ArgumentParser()
parser.add_argument("--date", type=parse)
args = parser.parse_args()

# Example usage
print(args.date) # prints datetime.datetime(2019, 5, 11, 0, 0)
```

## YYYY-MM-DD format
If your date format is fixed to YYYY-MM-DD, then you can use the `datetime.strptime()` method to convert the input string to a datetime object. Here's an example:

```python
import argparse
from datetime import datetime

parser = argparse.ArgumentParser()
parser.add_argument("--date", type=lambda x: datetime.strptime(x, '%Y-%m-%d'))
args = parser.parse_args()

# Example usage
print(args.date) # prints datetime.datetime(2019, 5, 11, 0, 0)
```

## DD/MM/YYYY format
To parse a date argument in the DD/MM/YYYY format, you can use the `datetime.strptime()` method as shown below:

```python
import argparse
from datetime import datetime

parser = argparse.ArgumentParser()
parser.add_argument("--date", type=lambda x: datetime.strptime(x, '%d/%m/%Y'))
args = parser.parse_args()

# Example usage
print(args.date) # prints datetime.datetime(2019, 5, 11, 0, 0)
``` 

## Unix timestamp format
Unix timestamp is a way to represent the number of seconds that have elapsed since January 1, 1970 (midnight UTC/GMT), also known as the Unix epoch. To parse a Unix timestamp argument, you can use the `datetime.fromtimestamp()` method as shown below:

```python
import argparse
from datetime import datetime

parser = argparse.ArgumentParser()
parser.add_argument("--date", type=lambda x: datetime.fromtimestamp(float(x)))
args = parser.parse_args()

# Example usage
print(args.date) # prints datetime.datetime(2019, 5, 11, 21, 45, 0)
```

Note that the Unix timestamp is assumed to be in UTC/GMT, so you may need to adjust it to your local timezone if necessary.
