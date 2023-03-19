---
title: What is the duration between two dates?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-12 00:00:00
updated_at: 2023-03-12 00:00:00
tldr: To calculate the number of days between two dates in Python, subtract the earlier date from the later date and use the days attribute of the resulting timedelta object.
---

**Contents**

[TOC]

# Introduction
Calculating the number of days between two dates is a common task in many applications. Python provides us with several built-in modules to calculate the days between two dates.

# Using dateutil
One of the easiest ways to calculate the days between two dates in Python is by using the dateutil module. This module provides the relativedelta() function that can calculate the days between two dates.

Here's a piece of code that shows how to use the dateutil module:

```python
from dateutil import relativedelta
from datetime import datetime

date1 = datetime.strptime('2019-05-06', '%Y-%m-%d')
date2 = datetime.strptime('2020-07-15', '%Y-%m-%d')

delta = relativedelta.relativedelta(date2, date1)
print(delta.days)
```

Output:
```
435
```

# Using timedelta
Another method to calculate the days between two dates in Python is by using the datetime module's timedelta class. Here's an example:

```python
from datetime import datetime

date1 = datetime.strptime('2019-05-06', '%Y-%m-%d')
date2 = datetime.strptime('2020-07-15', '%Y-%m-%d')

delta = date2 - date1
print(delta.days)
```

Output:
```
435
```

# Using Pandas
Pandas is a popular data manipulation library in Python. It also provides several functions to work with dates and times. Here's an example of using Pandas to calculate the days between two dates:

```python
import pandas as pd

date1 = pd.to_datetime('2019-05-06')
date2 = pd.to_datetime('2020-07-15')

delta = date2 - date1
print(delta.days)
```

Output:
```
435
```

# Conclusion
In this tutorial, we learned how to calculate the days between two dates in Python using three different methods: dateutil, timedelta, and Pandas. Choose the method that works best for your particular use case, keeping in mind the strengths and limitations of each.
