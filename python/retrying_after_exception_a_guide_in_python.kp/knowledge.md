---
title: What should be done if an exception occurs?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: You can use a try-except block with a loop to retry after an exception in Python.
---

**Contents**

[TOC]

# 1. Determine the Exception

The first step to retrying after an exception in Python is to determine the type of exception that was thrown. This can be done by using a `try-except` block to catch the exception and print out the type of exception.

```python
try:
    # code that may throw an exception
except Exception as e:
    print(type(e))
```

# 2. Determine the Retry Logic

Once the type of exception has been determined, the next step is to decide on the logic for retrying. This can vary depending on the type of exception and what the code is trying to accomplish. For example, if the code is trying to make a web request, it may make sense to retry after a few seconds if a connection timeout exception is thrown.

# 3. Implement the Retry Logic

Once the retry logic has been determined, it can be implemented using a `while` loop. Inside the `while` loop, the code that may throw an exception should be placed in a `try-except` block. If an exception is thrown, the retry logic can be implemented by using an `if` statement to check the type of exception and a `time.sleep()` call to delay the retry.

```python
while True:
    try:
        # code that may throw an exception
    except Exception as e:
        if type(e) == ConnectionTimeout:
            time.sleep(5)
        else:
            raise
```

# 4. Limit the Number of Retries

Finally, it is important to limit the number of retries that are attempted in order to prevent an infinite loop. This can be done by using a `for` loop and a counter variable to keep track of the number of retries. Once the counter reaches a certain limit, the loop can be broken out of.

```python
for i in range(5):
    try:
        # code that may throw an exception
    except Exception as e:
        if type(e) == ConnectionTimeout:
            time.sleep(5)
        else:
            raise
```
