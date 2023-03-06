---
title: Adjusting date ticks and rotation in matplotlib
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: To set the rotation of date ticks in Matplotlib in Python, use the `set\_rotation` method of the `xticks` object and the `DateFormatter` object to format the dates.
---

**Contents**

[TOC]

Section 1: Introduction
-----------------------
Matplotlib is a data visualization library for Python. It is widely used for creating various types of charts and graphs. In this tutorial, we will learn how to set date ticks and rotation in Matplotlib.

Section 2: Setting Date Ticks in Matplotlib
------------------------------------------
Matplotlib provides different ways to set date ticks. The easiest way is to use the `set_xticks` method. We can pass an array of datetime objects to this method to set the tick values.

```python
import matplotlib.pyplot as plt
import datetime as dt

dates = [dt.datetime(2021, 9, 1),
         dt.datetime(2021, 9, 15),
         dt.datetime(2021, 10, 1),
         dt.datetime(2021, 10, 15),
         dt.datetime(2021, 11, 1)]

values = [10, 20, 30, 40, 50]

plt.plot(dates, values)
plt.xticks(dates)
plt.show()
```

In the above code, we first import the necessary libraries, and then create two lists with dates and values. We then plot the data using the `plot` method of Matplotlib. After that, we use the `xticks` method to set the date ticks.

Section 3: Rotating Date Ticks in Matplotlib
--------------------------------------------
If we have a large number of dates, the date ticks may overlap and become unreadable. In such cases, we can rotate the date ticks to make them more readable. We can use the `set_xticklabels` method to rotate date ticks.

```python
import matplotlib.pyplot as plt
import datetime as dt

dates = [dt.datetime(2021, 9, 1),
         dt.datetime(2021, 9, 15),
         dt.datetime(2021, 10, 1),
         dt.datetime(2021, 10, 15),
         dt.datetime(2021, 11, 1)]

values = [10, 20, 30, 40, 50]

plt.plot(dates, values)
plt.xticks(rotation=45)
plt.show()
```

In the above code, we first import the necessary libraries, and then create two lists with dates and values. We then plot the data using the `plot` method of Matplotlib. After that, we use the `xticks` method to set the date ticks and the `rotation` parameter to specify the rotation angle in degrees.

Section 4: Conclusion
----------------------
In this tutorial, we learned how to set date ticks and rotate them in Matplotlib. By setting date ticks and rotating them, we can make our charts and graphs more readable and informative.
