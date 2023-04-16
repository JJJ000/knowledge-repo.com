---
title: Transforming epoch time into a readable date and time format
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: You can convert Epoch time into datetime in Python by using the datetime module`s fromtimestamp() method.
---

**Contents**

[TOC]

### Section 1: Understanding Epoch Time
Epoch time, also known as Unix time, is the number of seconds that have elapsed since midnight of January 1, 1970. It is widely used in computer systems to keep track of time.

### Section 2: Converting Epoch Time to Datetime
In Python, we can use the ```datetime``` module to convert Epoch time to datetime. To do this, we need to first create a ```datetime``` object with the Epoch time as an argument. We can then use the ```strftime()``` method to convert the ```datetime``` object to a string with the desired format.

### Section 3: Example Code
Below is an example of how to convert Epoch time to datetime in Python:

```
import datetime

# Create datetime object with Epoch time
epoch_time = 1577836800
dt = datetime.datetime.fromtimestamp(epoch_time)

# Convert datetime object to desired format
dt_formatted = dt.strftime('%Y-%m-%d %H:%M:%S')

# Print formatted datetime
print(dt_formatted)
```

### Section 4: Output
The output of the above code would be:

```
2020-01-01 00:00:00
```
