---
title: What is the difference in accuracy between python's time.clock() and time.time() functions?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-02 00:00:00
updated_at: 2023-02-02 00:00:00
tldr: time.clock() is more accurate on Windows, while time.time() is more accurate on Unix-based systems.
---

**Contents**

[TOC]

**time.clock()**

Accuracy:
time.clock() is typically accurate to the microsecond level on most modern platforms.

Limitations: 
time.clock() only measures the time spent in the current thread, and does not account for time spent in other threads. Additionally, time.clock() may return a different value on different platforms, as it is platform-dependent.

**time.time()**

Accuracy:
time.time() is typically accurate to the millisecond level on most modern platforms.

Limitations:
time.time() only measures the time since the epoch, and does not account for time spent in other threads. Additionally, time.time() may return a different value on different platforms, as it is platform-dependent.
