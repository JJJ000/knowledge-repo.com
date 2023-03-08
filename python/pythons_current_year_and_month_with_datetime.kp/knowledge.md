---
title: How to get the current year and month in Python using datetime?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-08 00:00:00
updated_at: 2023-03-08 00:00:00
tldr: To get the current year and month in Python, you can use the datetime module and call the now() method, followed by the strftime() method with the format specifier `%Y` for the year and `%m` for the month.
---

**Contents**

[TOC]

# Introduction
In Python, we can easily get the current year and month using the built-in datetime module. This module provides various classes for working with dates and times. In this article, we will see how to get the current year and month in Python.

# Getting Current Year
To get the current year in Python, we can use the `datetime` class from the datetime module. The `datetime` class has a `now()` method that returns the current date and time. We can extract the year from the current date using the `year` attribute.

```python
from datetime import datetime

current_year = datetime.now().year
print(current_year)
```

Output:
```
2022
```

# Getting Current Month
Similar to getting the current year, we can get the current month using the `month` attribute of the `datetime` class.

```python
from datetime import datetime

current_month = datetime.now().month
print(current_month)
```

Output:
```
7
```

# Getting Current Year and Month Together
We can combine the above two approaches to get the current year and month together in a single statement.

```python
from datetime import datetime

current_year, current_month = datetime.now().year, datetime.now().month
print(current_year, current_month)
```

Output:
```
2022 7
```

# Conclusion
In this article, we saw how to get the current year and month in Python using the datetime module. We can use the `year` and `month` attributes of the `datetime` class to get the respective values.
