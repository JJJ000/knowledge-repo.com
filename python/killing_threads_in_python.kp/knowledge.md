---
title: Is it possible to terminate a thread?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-30 00:00:00
updated_at: 2023-04-30 00:00:00
tldr: Yes, the built-in function threading.Thread.join() can be used to terminate a thread in Python.
---

**Contents**

[TOC]

1. Killing a Thread with `thread.exit()`
---------------------------------------
Python's `thread` module provides a `thread.exit()` method to terminate threads. This method raises an exception in the thread, which will cause the thread to exit.

2. Killing a Thread with `thread.interrupt_main()`
--------------------------------------------------
Python's `thread` module also provides a `thread.interrupt_main()` method, which can be used to terminate the main thread. This method raises a `KeyboardInterrupt` exception in the main thread, which can be handled by the application.

3. Killing a Thread with `thread.cancel()`
-----------------------------------------
Python's `thread` module also provides a `thread.cancel()` method, which can be used to terminate a thread. This method raises an exception in the thread, which will cause the thread to exit.

4. Killing a Thread with `os.kill()`
------------------------------------
The `os` module provides a `os.kill()` method, which can be used to terminate a thread. This method sends a signal to the thread, which will cause the thread to exit.
