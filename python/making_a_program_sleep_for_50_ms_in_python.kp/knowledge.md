---
title: What is the code to make my program pause for 50 milliseconds?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-30 00:00:00
updated_at: 2023-04-30 00:00:00
tldr: Use the time.sleep(0.05) function.
---

**Contents**

[TOC]

# Using time.sleep()
The most straightforward way to make a program sleep for 50 milliseconds in Python is to use the `time.sleep()` method. This method pauses the program for a specified amount of time, in this case 50 milliseconds.

```
import time
time.sleep(0.05)
```

# Using threading.Timer
Another way to make a program sleep for 50 milliseconds in Python is to use the `threading.Timer` class. This class creates a timer that can be used to call a function after a specified amount of time, in this case 50 milliseconds.

```
import threading
timer = threading.Timer(0.05, my_function)
timer.start()
```

# Using select.select()
A third way to make a program sleep for 50 milliseconds in Python is to use the `select.select()` method. This method pauses the program until a specified amount of time has elapsed, in this case 50 milliseconds.

```
import select
select.select([], [], [], 0.05)
```
