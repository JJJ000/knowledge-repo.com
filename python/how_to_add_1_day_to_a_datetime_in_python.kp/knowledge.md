---
title: What is the process of increasing one day to a datetime?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: Use timedelta function from datetime module to increment a datetime by one day in Python.
---

**Contents**

[TOC]

Section 1: Introduction

In this tutorial, we will learn how to increment a datetime object in Python by one day. Datetime is a module in Python that is used for working with dates and times. It provides classes for working with both dates and times together. 

Section 2: Using timedelta to increment datetime object by one day

One way to increment a datetime object by one day is by using the timedelta class from the datetime module. timedelta represents a duration or difference between two dates or times. We can use this class to increment a datetime object by one day. Here is an example of how to do it:

```python
from datetime import datetime, timedelta

date = datetime(2022, 2, 1)
one_day = timedelta(days=1)
new_date = date + one_day

print("Original Date:", date)
print("New Date:", new_date)
```

Output:
```
Original Date: 2022-02-01 00:00:00
New Date: 2022-02-02 00:00:00
```

In this example, the datetime object `date` represents February 1, 2022. We create a timedelta object `one_day` with the argument `days=1`, which represents a duration of one day. We then add the timedelta object to the `date` object using the `+` operator, which returns a new datetime object `new_date` representing February 2, 2022.

Section 3: Using the datetime library to increment datetime object by one day

Another way to increment a datetime object by one day is to use the `datetime` library. We can use the `datetime` library's `date()` and `timedelta()` methods to create a new date object and increment it by one day. Here is an example of how to do it:

```python
from datetime import datetime, timedelta

date = datetime(2022, 2, 1)
new_date = (date + timedelta(days=1)).date()

print("Original Date:", date)
print("New Date:", new_date)
```

Output:
```
Original Date: 2022-02-01 00:00:00
New Date: 2022-02-02
```

In this example, we create a datetime object `date` representing February 1, 2022. We then add a timedelta object with the argument `days=1`, which gives us a duration of one day. Finally, we call the `date()` method on the resulting datetime object to extract just the date part and assign it to `new_date`.

Section 4: Conclusion

In this tutorial, we learned two ways to increment a datetime object in Python by one day. The first method involved using the `timedelta` class from the datetime library, while the second method involved using the `datetime` library's `date()` and `timedelta()` methods. Both methods are valid and have their use cases, depending on the specific needs of the program.
