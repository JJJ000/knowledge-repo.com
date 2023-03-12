---
title: What's the method to generate a datetime object that denotes a time 15 minutes earlier?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-12 00:00:00
updated_at: 2023-03-12 00:00:00
tldr: Use the datetime module to subtract 15 minutes from the current time using timedelta. 

```python
from datetime import datetime, timedelta
fifteen\_minutes\_ago = datetime.now() - timedelta(minutes=15)
```
---

**Contents**

[TOC]

## Importing Necessary Modules

To work with dates and times in Python, we need the datetime module. Therefore, we need to import that in our code.

```python
from datetime import datetime, timedelta
```

## Datetime Calculation

To calculate the datetime that is 15 minutes ago, we can use the timedelta function from Python's datetime module. Here is the code snippet:

```python
# create a datetime object for the current time
current_time = datetime.now()

# define a timedelta object for 15 minutes
time_difference = timedelta(minutes=15)

# subtract the time difference from the current time
time_15_minutes_ago = current_time - time_difference

# output the datetime object
print(time_15_minutes_ago)
```

In this code snippet, we first create a datetime object for the current time. Then, we define a timedelta object for 15 minutes, which we then subtract from the current time to get the datetime that is 15 minutes ago.


## Complete Code

Here is the complete code that can be used to create a datetime object for 15 minutes ago in Python:

```python
from datetime import datetime, timedelta

# create a datetime object for the current time
current_time = datetime.now()

# define a timedelta object for 15 minutes
time_difference = timedelta(minutes=15)

# subtract the time difference from the current time
time_15_minutes_ago = current_time - time_difference

# output the datetime object
print(time_15_minutes_ago)
```

This code will output the datetime that is 15 minutes ago from the current time.
