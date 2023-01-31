---
title: What is the standard output generated when running pytest?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-01-30 00:00:00
updated_at: 2023-01-30 00:00:00
tldr: You can use the `-s` option when running pytest to see normal print output.
---

**Contents**

[TOC]

**1. Using the -s Option**

The simplest way to view print output created during a pytest run is to use the -s option when running pytest. This option will cause all print statements to be displayed in the console window, allowing you to see the output.

**2. Using the -v Option**

Another option is to use the -v option when running pytest. This will enable verbose mode, which will display more detailed information about the test run, including any print statements.

**3. Using the --capture=no Option**

The --capture=no option can be used to disable capturing of output from print statements. This will allow you to see the output in the console window.

**4. Using a Logging Module**

Finally, you can use a logging module to capture the output from print statements. This will allow you to view the output in a log file, which can be useful for debugging purposes.
