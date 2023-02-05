---
title: What kind of exception happened?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: You can determine what type of exception occurred in Python by inspecting the exception object`s type attribute.
---

**Contents**

[TOC]

# 1. Examine the Traceback 
When an exception occurs, Python will display an error message with a traceback that shows the line of code where the exception occurred. Examining this traceback can give you an indication of the type of exception that occurred.

# 2. Check the Documentation 
The official Python documentation includes a list of built-in exceptions. You can check this list to see if the exception you encountered is listed. If it is, you can read the description of the exception to get more information about it.

# 3. Catch Specific Exceptions 
You can use the try/except statement to catch specific types of exceptions. This allows you to handle different types of exceptions differently. You can also use this to get more information about the type of exception that occurred.

# 4. Use the Type Function 
You can use the type() function to determine the type of an exception. This function will return the type of the exception, which can be used to determine the type of exception that occurred.
