---
title: What is the formula for determining the number of days between two given dates?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-30 00:00:00
updated_at: 2023-04-30 00:00:00
tldr: You can use the datetime.timedelta() method to calculate the number of days between two given dates in Python.
---

**Contents**

[TOC]

# Section 1: Import Necessary Libraries

The first step is to import any necessary libraries. In this case, we will need the `datetime` library from the Python Standard Library.

```python
import datetime
```

# Section 2: Define the Dates

Next, we need to define the two dates that we want to calculate the number of days between. We can do this by creating two `datetime` objects.

```python
date1 = datetime.date(2020, 5, 15)
date2 = datetime.date(2020, 6, 20)
```

# Section 3: Calculate the Difference

We can now calculate the difference between the two dates using the `timedelta` method from the `datetime` library. 

```python
difference = date2 - date1
```

# Section 4: Output the Result

Finally, we can output the result by printing out the `difference` variable.

```python
print(difference.days)
```

The output of this code will be `36`, which is the number of days between the two dates.
