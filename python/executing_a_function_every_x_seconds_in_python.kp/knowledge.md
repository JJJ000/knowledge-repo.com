---
title: What is the best way to set up a function to run every x seconds?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-02 00:00:00
updated_at: 2023-02-02 00:00:00
tldr: Use the time.sleep() function to execute a function every x seconds.
---

**Contents**

[TOC]

### Using Time Module

The `time` module provides various time-related functions. It can be used to set a timer and execute a function after a certain period of time.

```python
import time

def execute_function():
    # code to execute

while True:
    execute_function()
    time.sleep(x) # x is the number of seconds
```

### Using Threading Module

The `threading` module provides a Timer class that can be used to execute a function after a certain period of time.

```python
import threading

def execute_function():
    # code to execute

timer = threading.Timer(x, execute_function) # x is the number of seconds
timer.start()
```

### Using Scheduling Module

The `scheduling` module provides a scheduler class that can be used to execute a function periodically.

```python
import scheduling

def execute_function():
    # code to execute

scheduler = scheduling.scheduler(time.time, time.sleep)
scheduler.enter(x, 1, execute_function) # x is the number of seconds
scheduler.run()
```

### Using Loop

The simplest way to execute a function every x seconds is to use a while loop.

```python
def execute_function():
    # code to execute

while True:
    execute_function()
    time.sleep(x) # x is the number of seconds
```
