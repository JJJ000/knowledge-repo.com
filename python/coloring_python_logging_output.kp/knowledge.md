---
title: What is the best way to add color to Python logging output?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Use the `logging.Formatter` class to format the logging output with ANSI escape sequences.
---

**Contents**

[TOC]

1. Using Colorama
------------------------
[Colorama](https://pypi.org/project/colorama/) is a cross-platform Python library for colored terminal text. It can be used to color Python logging output.

2. Using Logging Formatter
------------------------
The [logging.Formatter](https://docs.python.org/3/library/logging.html#logging.Formatter) class in the Python standard library can be used to format logging output and add color to it.

3. Using Logging Handler
------------------------
The [logging.Handler](https://docs.python.org/3/library/logging.html#logging.Handler) class in the Python standard library can be used to add color to logging output.

4. Using Third-Party Libraries
------------------------
There are also several third-party libraries such as [colorlog](https://pypi.org/project/colorlog/) and [coloredlogs](https://pypi.org/project/coloredlogs/) that can be used to color Python logging output.
