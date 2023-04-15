---
title: What is a way to increase the datetime by a specific number of months in python, without resorting to using any external libraries?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-16 00:00:00
updated_at: 2023-04-16 00:00:00
tldr: Create a custom function that adds the desired number of months to a datetime object using the `.replace()` method.
---

**Contents**

[TOC]

### Step 1: Get the current date and time

We first need to get the current date and time using the datetime module. We can use the `datetime.datetime.now()` function to get the current date and time. We will also define a variable `custom_months` which will define the number of months to increment the datetime object.

```python
import datetime

current_datetime = datetime.datetime.now()
custom_months = 3
```

### Step 2: Calculate the new month and year

We will calculate the new month and year after incrementing the custom number of months. We will use the `timedelta` function which is a class in the datetime module. We can add the custom number of months to the current month and take the modulus of 12 to get the new month. We will also calculate the new year by adding the quotient of the custom number of months and 12 to the current year.

```python
new_month = (current_datetime.month + custom_months) % 12
new_year = current_datetime.year + (current_datetime.month + custom_months) // 12
```

### Step 3: Create the new datetime object

Now that we have the new month and year, we can create a new datetime object using the `datetime.datetime()` function. We will pass the new year, new month, current day, current hour, current minute and current second as parameters to the function.

```python
new_datetime = datetime.datetime(new_year, new_month, current_datetime.day, 
                                  current_datetime.hour, current_datetime.minute, 
                                  current_datetime.second)
```

### Step 4: Display the new datetime object

Finally, we can display the new datetime object using the `strftime()` function. This function is used to format the datetime object into a string that can be displayed to the user. We will pass the desired format as a parameter to the function. 

```python
print(new_datetime.strftime("%Y-%m-%d %H:%M:%S"))
```

The final code would look like this:

```python
import datetime

current_datetime = datetime.datetime.now()
custom_months = 3

new_month = (current_datetime.month + custom_months) % 12
new_year = current_datetime.year + (current_datetime.month + custom_months) // 12

new_datetime = datetime.datetime(new_year, new_month, current_datetime.day, 
                                  current_datetime.hour, current_datetime.minute, 
                                  current_datetime.second)

print(new_datetime.strftime("%Y-%m-%d %H:%M:%S"))
``` 

This code will increment the datetime by 3 months and display the new date and time in "YYYY-MM-DD HH:MM:SS" format.
