---
title: What is the runtime of a Python program?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: You can use the time module to get the time of a Python program`s execution.
---

**Contents**

[TOC]

1. Using the `time` Module

The `time` module provides a number of functions that can be used to measure the execution time of a Python program. To get the total execution time of a program, you can use the `time.time()` function. This function returns the number of seconds since the Unix epoch (January 1, 1970).

To get the total execution time of a program, you can use the following code:

```
import time
start_time = time.time()
# Run program code here
end_time = time.time()
total_time = end_time - start_time
```

2. Using the `timeit` Module

The `timeit` module provides a number of functions that can be used to measure the execution time of a Python program. The `timeit.timeit()` function can be used to get the total execution time of a program. This function takes a parameter that specifies the number of times the code should be executed.

To get the total execution time of a program, you can use the following code:

```
import timeit
start_time = timeit.timeit()
# Run program code here
end_time = timeit.timeit()
total_time = end_time - start_time
```

3. Using the `datetime` Module

The `datetime` module provides a number of functions that can be used to measure the execution time of a Python program. The `datetime.datetime.now()` function can be used to get the current date and time. This function returns a `datetime` object that contains the current date and time.

To get the total execution time of a program, you can use the following code:

```
import datetime
start_time = datetime.datetime.now()
# Run program code here
end_time = datetime.datetime.now()
total_time = end_time - start_time
```

4. Using the `timeit` Context Manager

The `timeit` module also provides a context manager that can be used to measure the execution time of a Python program. The `timeit.Timer()` context manager can be used to measure the execution time of a program. This context manager takes a parameter that specifies the number of times the code should be executed.

To get the total execution time of a program, you can use the following code:

```
import timeit
with timeit.Timer() as timer:
    # Run program code here
total_time = timer.interval
```
