---
title: What is the process to include additional hours to the present time using python?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: You can use the datetime module in Python and add hours to the current time using the timedelta method.
---

**Contents**

[TOC]

# Introduction
In Python, you can easily add hours to the current time using the datetime module. This module provides various classes for working with dates and times, including classes for working with time zones.

# Step 1: Import datetime module
The first step is to import the datetime module in your Python script.

```python
import datetime
```

# Step 2: Get the current time
Next, you need to get the current time using the `datetime.now()` function.

```python
current_time = datetime.datetime.now()
```

# Step 3: Add hours to the current time
Now you can add hours to the current time using the `datetime.timedelta()` function. This function takes a number of arguments, including the number of days, seconds, microseconds, and milliseconds.

```python
hours_added = datetime.timedelta(hours=3)
new_time = current_time + hours_added
```

In this example, we added 3 hours to the current time.

# Conclusion
That's it! You have successfully added hours to the current time in Python using the datetime module.
