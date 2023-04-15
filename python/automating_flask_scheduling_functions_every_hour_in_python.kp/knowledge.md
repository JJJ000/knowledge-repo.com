---
title: How can a function be scheduled to run every hour in flask?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Use a scheduler library like `APScheduler` to schedule the function to run every hour.
---

**Contents**

[TOC]

## Import Required Libraries

Firstly, we need to import the `datetime` module to make use of the `datetime` function that will help us schedule a function to run every hour at a specific time. We will also need the `time` module to add a delay between each hour.


## Define the Function

Next, we need to define the function that needs to run every hour. In this example, we will print the current time.


## Use a While Loop to Schedule the Function

Lastly, we will use a `while` loop to schedule the function to run every hour. We will set a delay of 60 minutes (1 hour) using the `time.sleep()` function. The while loop will continue running indefinitely, executing the function every hour.

```python

import datetime
import time
from flask import Flask

app = Flask(__name__)

def hourly_job():
    print("The current time is", datetime.datetime.now())

if __name__ == '__main__':
    while True:
        # get the current time
        current_time = datetime.datetime.now().time()
        # check if the current time is at the start of the hour
        # i.e. when minutes and seconds are zero
        if current_time.minute == 0 and current_time.second == 0:
            hourly_job()
            # wait for 60 minutes (1 hour)
            time.sleep(60*60)

``` 

This example shows how to schedule a function to run every hour. We used the `datetime` and `time` modules to schedule and delay the function execution. We used a while loop to continuously check if it's the start of a new hour and called the function if so.
