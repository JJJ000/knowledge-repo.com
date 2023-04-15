---
title: Performing recurring tasks
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: You can use Python`s built-in `time` module, or a third-party library like `schedule`, to execute periodic actions in Python.
---

**Contents**

[TOC]

1. Introduction to Periodic Actions
Periodic actions are actions that are executed at regular intervals. In Python, there are several mechanisms that can be used to implement periodic actions. These range from the use of the time module and the sched module, to the use of external libraries like schedule or apscheduler.

2. Using the time.sleep() function
The simplest way to implement periodic actions in Python is by using the time module. The time.sleep() function, when called with a positive integer or float value as an argument, causes the program to pause for the specified number of seconds. By using a loop and calling time.sleep() at the end of each iteration, it is possible to create a simple periodic action.
```python
import time

while True:
    # execute some action
    time.sleep(60)  # pause for 60 seconds
```

3. Using the sched module
The sched module provides a more sophisticated way of implementing periodic actions. The module contains a scheduler class that can be used to schedule events at specific times or at regular intervals. To schedule periodic events using the sched module, you first create a scheduler object, then use the scheduler.enter() method to schedule the event at the desired interval.
```python
import sched
import time

def periodic_action(sc):
    # execute some action
    sc.enter(60, 1, periodic_action, (sc,))  # reschedule the event to occur in 60 seconds

s = sched.scheduler(time.time, time.sleep)
s.enter(60, 1, periodic_action, (s,))
s.run()
```

4. Using external libraries
There are several external libraries that can be used to implement periodic actions in Python. Two popular ones are schedule and apscheduler. These libraries simplify the process of scheduling periodic events by providing easy-to-use interfaces and additional features like the ability to specify time zones and to schedule events using human-readable syntax.
```python
import schedule
import time

def periodic_action():
    # execute some action

schedule.every(1).minutes.do(periodic_action)

while True:
    schedule.run_pending()
    time.sleep(1)
```
```python
from apscheduler.schedulers.blocking import BlockingScheduler

def periodic_action():
    # execute some action

scheduler = BlockingScheduler()
scheduler.add_job(periodic_action, 'interval', minutes=1)
scheduler.start()
```
