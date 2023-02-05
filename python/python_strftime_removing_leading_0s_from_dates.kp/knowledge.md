---
title: What is the syntax for formatting a date without a leading zero in Python using the strftime function?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: The %-d format specifier can be used to format a date without a leading 0.
---

**Contents**

[TOC]

# Section 1: Overview

Python strftime() is a built-in function in the datetime module that is used to convert a datetime object to a string according to a given format. It takes in a format string as an argument, which specifies the format in which the output should be presented.

# Section 2: Date Without Leading 0

The strftime() function allows for the formatting of dates without leading zeroes. To do this, use the '%e' flag, which will print the day of the month as a single digit if it is less than 10. For example, if the day of the month is 8, the output will be 8 instead of 08.

# Section 3: Example

For example, the following code will print the date as "9/15/20":

```
from datetime import datetime

date = datetime(2020, 9, 15)
print(date.strftime('%e/%m/%y'))
```

# Section 4: Conclusion

In conclusion, Python strftime() is a convenient way to format dates without leading zeroes. To do this, use the '%e' flag, which will print the day of the month as a single digit if it is less than 10.
