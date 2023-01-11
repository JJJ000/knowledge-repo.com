---
title: What is the best way to create a time delay?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-01-11 00:00:00
updated_at: 2023-01-11 00:00:00
tldr: You can use the `time.sleep()` function to delay execution of code for a certain amount of time.
---

**Contents**

[TOC]

### Using the `time` Module 
The `time` module provides various time-related functions, including a function for waiting a specified amount of time. 

### Example
```python
import time

# Delay for 5 seconds
time.sleep(5)
```

### Using the `datetime` Module
The `datetime` module provides various time-related functions, including a function for calculating the difference between two dates. 

### Example
```python
from datetime import datetime

# Delay for 5 seconds
start_time = datetime.now()
while (datetime.now() - start_time).seconds < 5:
    pass
```
