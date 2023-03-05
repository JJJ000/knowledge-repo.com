---
title: How to format the date in Python for yesterday's date?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-05 00:00:00
updated_at: 2023-03-05 00:00:00
tldr: Using the `datetime` module in Python, you can format yesterday`s date by subtracting a day from today`s date and using the `strftime` function with the desired format.
---

**Contents**

[TOC]

Section 1: Introduction
In Python, dates can be formatted using the datetime module. The datetime module provides various functions to format dates according to our requirements. One such requirement could be formatting yesterday's date.

Section 2: Importing datetime module
To format yesterday's date in Python, we first need to import the datetime module. We can do this using the below code snippet:
```python
import datetime
```

Section 3: Formatting yesterday's date
Once we have imported the datetime module, we can use the date.today() function to get today's date and then minus one day from it using timedelta() function. After that we can format the date using strftime() function to get a string of yesterday's date in the desired format. 

```python
import datetime

today = datetime.date.today()
yesterday = today - datetime.timedelta(days=1)
formatted_yesterday = yesterday.strftime('%m-%d-%Y')
print(formatted_yesterday)
```

In the above code, we first get today's date using date.today() function, then we minus one day from it using timedelta() function and store it in yesterday variable. Finally, we format the date using strftime() function and store it in formatted_yesterday variable. 

The strftime() function takes a format string as an argument and returns a string representing the date in the specified format. The '%m-%d-%Y' format string means that the date should be represented as a month-day-year format, for example, '04-05-2022'. 

Section 4: Conclusion
In this tutorial, we have seen how to format yesterday's date using the datetime module in Python. We used the date.today() function to get today's date and then minus one day from it using timedelta() function. Finally, we formatted the date using strftime() function to get a string of yesterday's date in the desired format.
