---
title: What is the best way to escape percent (%) signs in Python strings?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Use `%%` to escape a single percent character in a Python string.
---

**Contents**

[TOC]

**Using the Percent Sign (%)**

1. Prefix the percent sign with a backslash (\\):
   ```python
   my_string = "100% of the time"
   print(my_string) # Output: 100% of the time
   print("\%s" % my_string) # Output: %100 of the time
   ```

2. Use the string.replace() method:
   ```python
   my_string = "100% of the time"
   print(my_string) # Output: 100% of the time
   print(my_string.replace("%", "\%")) # Output: 100\% of the time
   ```

**Using the Format Method**

1. Use the format method:
   ```python
   my_string = "100% of the time"
   print(my_string) # Output: 100% of the time
   print("{0:s}".format(my_string)) # Output: 100% of the time
   ```

2. Use the format method with the percent sign (%):
   ```python
   my_string = "100% of the time"
   print(my_string) # Output: 100% of the time
   print("{0:s}".format("%" + my_string)) # Output: %100 of the time
   ```
