---
title: What type of timestamp does python's time.time() function return - local or utc?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-01 00:00:00
updated_at: 2023-02-01 00:00:00
tldr: Python`s time.time() returns the local timestamp.
---

**Contents**

[TOC]

# Local Time
Python's time.time() returns the local timestamp.

# Examples
For example, if the local time is currently 14:00 UTC, time.time() will return 14:00.

# Time Zones
The time returned by time.time() is based on the local time zone. If the local time zone is changed, the value returned by time.time() will also be changed.

# UTC
However, the time returned by time.time() is not in UTC. To get the UTC timestamp, use the time.gmtime() function.
