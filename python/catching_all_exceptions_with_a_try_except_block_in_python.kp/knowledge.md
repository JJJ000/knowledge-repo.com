---
title: What is the syntax for writing a "try"/"except" block that catches all exceptions?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-01-30 00:00:00
updated_at: 2023-01-30 00:00:00
tldr: `Try <code>except Exception</code>`
---

**Contents**

[TOC]

1. # Setting up the `try`/`except` Block

```python
try:
    # code that may cause an exception
except:
    # code to be executed if an exception occurs
```

2. # Catching All Exceptions

```python
try:
    # code that may cause an exception
except Exception as e:
    # code to be executed if an exception occurs
    print(e)
```

3. # Handling the Exception

```python
try:
    # code that may cause an exception
except Exception as e:
    # code to be executed if an exception occurs
    print(e)
    # code to handle the exception
```

4. # Finishing the `try`/`except` Block

```python
try:
    # code that may cause an exception
except Exception as e:
    # code to be executed if an exception occurs
    print(e)
    # code to handle the exception
else:
    # code to be executed if no exception occurs
finally:
    # code to be executed regardless of whether an exception occurs
```
