---
title: Converting a Python datetime object to a string without the microsecond component
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-01 00:00:00
updated_at: 2023-02-01 00:00:00
tldr: Use the strftime() method to format a datetime object as a string without microseconds.
---

**Contents**

[TOC]

#### Formatting a DateTime Object

The `datetime` object in Python can be formatted into a readable string by using the `strftime()` method. The syntax of this method is `datetime_object.strftime(format)`, where `format` is a string containing the desired format of the output string.

#### Removing the Microsecond Component

The microsecond component of a `datetime` object can be removed by using the `replace()` method. This method takes two arguments, the first being the microsecond to replace the existing microsecond with, and the second being the value to replace it with.

#### Example

The following example shows how to convert a `datetime` object to a string without the microsecond component.

```python
from datetime import datetime

# Create a datetime object
dt = datetime(2020, 7, 15, 10, 45, 30, 123456)

# Remove the microsecond component
dt_no_microsecond = dt.replace(microsecond=0)

# Convert the datetime object to a string
dt_string = dt_no_microsecond.strftime('%Y-%m-%d %H:%M:%S')

# Print the string
print(dt_string)
# Output: 2020-07-15 10:45:30
```
