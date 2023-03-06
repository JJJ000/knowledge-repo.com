---
title: What is the method to determine the time difference between two time strings?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: Convert the time strings to datetime objects using datetime.strptime and then subtract the earlier datetime object from the later datetime object to get the time interval.
---

**Contents**

[TOC]

Section 1: Introduction
Python provides several built-in methods to handle time and date-related operations. In this tutorial, we'll explore how to calculate the time interval between two time strings in Python. We'll use the 'datetime' module to help us with this task.

Section 2: Get the time difference using timedelta
The 'datetime' module in Python provides a 'datetime' class that represents a date and time object. It also provides a 'timedelta' class that represents the difference between two dates or times. We can use these classes to calculate the time interval between two time strings.

The following code snippet demonstrates how to do this:

```python
from datetime import datetime

time1 = datetime.strptime('2022-10-12 07:15:00', '%Y-%m-%d %H:%M:%S')
time2 = datetime.strptime('2022-10-12 08:45:00', '%Y-%m-%d %H:%M:%S')

difference = time2 - time1
print(difference)
```

Output:
```
1:30:00
```

In the above code, we first convert the time strings to datetime objects using the 'strptime' method. We then subtract the two datetime objects to get a timedelta object representing the time difference between the two dates.

Section 3: Format the time difference output
The timedelta object has several attributes that we can use to extract different components of the time difference. For example, we can use the 'days', 'seconds', and 'microseconds' attributes to extract the number of days, seconds, and microseconds between two dates. 

The following code snippet demonstrates how to format the output of the time difference in a human-readable format:

```python
from datetime import datetime

time1 = datetime.strptime('2022-10-12 07:15:00', '%Y-%m-%d %H:%M:%S')
time2 = datetime.strptime('2022-10-12 08:45:00', '%Y-%m-%d %H:%M:%S')

difference = time2 - time1

total_seconds = difference.total_seconds()
hours, remainder = divmod(total_seconds, 3600)
minutes, seconds = divmod(remainder, 60)

print('Time difference: {} hours, {} minutes, {} seconds'.format(int(hours), int(minutes), int(seconds)))
```

Output:
```
Time difference: 1 hours, 30 minutes, 0 seconds
```

In the above code, we first calculate the total number of seconds in the timedelta object using the 'total_seconds' method. We then use the 'divmod' function to extract the number of hours, minutes, and seconds between the two dates. Finally, we format the output in a human-readable format.

Section 4: Conclusion
In this tutorial, we learned how to calculate the time interval between two time strings in Python using the 'datetime' and 'timedelta' classes. We also learned how to format the output of the time difference in a human-readable format. I hope this tutorial has been helpful.
