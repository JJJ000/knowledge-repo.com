---
title: Does time.sleep cause a thread or process to pause?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-02 00:00:00
updated_at: 2023-02-02 00:00:00
tldr: The sleep() function can be used to pause both the thread and the process in Python.
---

**Contents**

[TOC]

# Thread

When using the `time.sleep` function, the current thread will be put to sleep, meaning that other threads will continue to execute.

# Process

When using the `time.sleep` function, the current process will be put to sleep, meaning that other processes will continue to execute.
