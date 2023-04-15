---
title: What is the Python code to get the current time in milliseconds?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-30 00:00:00
updated_at: 2023-04-30 00:00:00
tldr: You can get the current time in milliseconds in Python using the time.time() function.
---

**Contents**

[TOC]

# Section 1: Importing Library

In order to get the current time in milliseconds, we need to import the `datetime` library.

```python
import datetime
```

# Section 2: Get Current Time

Using the `datetime` library, we can get the current time in the form of a `datetime` object.

```python
current_time = datetime.datetime.now()
```

# Section 3: Convert to Milliseconds

The `datetime` object has a `timestamp()` method which returns the time in milliseconds.

```python
milliseconds = current_time.timestamp()
```

# Section 4: Print Milliseconds

Finally, we can print the current time in milliseconds.

```python
print(milliseconds)
```
