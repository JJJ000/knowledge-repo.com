---
title: What is the method to include the period (am/pm) in strftime?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-07 00:00:00
updated_at: 2023-03-07 00:00:00
tldr: To account for period (AM/PM) using strftime in Python, use the `%p` specifier.
---

**Contents**

[TOC]

### Introduction

In Python, the `strftime` method is used to format date and time strings according to specified format codes. This method takes the format string as input and returns a string representation of the date and time.

However, the `strftime` method does not directly support the display of the period (AM/PM) in the output string. In this article, we will explore different methods to account for period using `strftime` in Python.


### Method 1 - Using %p Format Code

One way to account for the period in the output string is to use the `%p` format code in the format string. This code returns the local equivalent of the AM/PM designation.

Here is an example code snippet:

```
import datetime

now = datetime.datetime.now()
formatted_time = now.strftime("%H:%M:%S %p")
print("Formatted Time:", formatted_time)
```

Output:
```
Formatted Time: 03:30:15 PM
```

Here, we have used `%p` format code in the format string to display AM/PM designation in the output string.

### Method 2 - Using strftime with time.struct_time

Another way to account for period in the output string is to use `time.struct_time` along with `strftime`. We can extract the `tm_hour` value from the `time.struct_time` object and manually add the period in the output string.

Here is an example code snippet:

```
import time

now = time.localtime()
hour = now.tm_hour
if hour < 12:
    period = "AM"
else:
    period = "PM"
    
formatted_time = time.strftime("%I:%M:%S ", now) + period
print("Formatted Time:", formatted_time)
```

Output:
```
Formatted Time: 03:30:15 PM
```

Here, we have used `time.localtime()` method to get the current local time. We have extracted the `tm_hour` value from the `time.struct_time` object and checked whether it is before or after 12 PM. Based on that, we manually added the period (AM/PM) in the output string.

### Conclusion

In this article, we have explored different methods to account for period (AM/PM) using `strftime` in Python. The first method uses `%p` format code in the format string, while the second method uses `time.struct_time` to manually add the period in the output string. Both methods are useful and can be used depending on the requirements.
