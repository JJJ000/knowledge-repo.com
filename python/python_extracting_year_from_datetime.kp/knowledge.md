---
title: What is the method to obtain the year from a Python datetime object?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-12 00:00:00
updated_at: 2023-03-12 00:00:00
tldr: Use the .year method on the datetime object.
---

**Contents**

[TOC]

Section 1: Introduction
Python’s datetime object is a powerful tool for working with dates and times in a python code. We can use this object to store and manipulate dates and time as per our requirement. In this tutorial, we will learn how to extract the year from the python datetime object.

Section 2: Using strftime() method
The datetime object in Python has a method called strftime() that can be used for formatting a date in a specific format. It takes a formatting string as an input and returns the date in the requested format. We can use the "%Y" format code to extract the year from the datetime object. The following example demonstrates how to extract the year from a datetime object using the strftime() method:

```Python
import datetime

my_date = datetime.datetime.now()
year = my_date.strftime("%Y")
print(year)
```

Output:
```
2022
```

In the above example, we first create a datetime object using the now() method of the datetime module. Then we call the strftime() method with the "%Y" format code and store the year value returned by the method in the year variable. Finally, we print the year value on the console.

Section 3: Using year attribute
The datetime object in python has a year attribute that returns the year value of the datetime object. We can use this attribute to extract the year value from the datetime object. The following example demonstrates how to extract the year from a datetime object using the year attribute:

```Python
import datetime

my_date = datetime.datetime.now()
year = my_date.year
print(year)
```

Output:
```
2022
```

In the above example, we first create a datetime object using the now() method of the datetime module. Then we access the year attribute of the datetime object and store the year value in the year variable. Finally, we print the year value on the console.

Section 4: Conclusion 
In this tutorial, we discussed how to extract the year from a python datetime object. We learned two methods for extracting the year from the datetime object, namely using the strftime() method and the year attribute of the datetime object. We hope that this tutorial will help you in your python datetime operations.
