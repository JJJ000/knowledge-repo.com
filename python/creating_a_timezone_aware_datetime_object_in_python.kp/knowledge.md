---
title: What is the process for creating a datetime object that takes into account different time zones?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Create a datetime object in the desired timezone using the datetime.now(tz=timezone) method.
---

**Contents**

[TOC]

## Creating a Timezone Aware Datetime Object

1. Import the `datetime` module and the `pytz` module:
    ```python
    import datetime
    import pytz
    ```

2. Create a `datetime` object with the desired date and time:
    ```python
    dt = datetime.datetime(2020, 6, 15, 12, 0, 0)
    ```

3. Create a `pytz` timezone object for the desired timezone:
    ```python
    tz = pytz.timezone('US/Eastern')
    ```

4. Use the `localize` method of the `pytz` timezone object to create a timezone aware datetime object:
    ```python
    dt_tz = tz.localize(dt)
    ```
