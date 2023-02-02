---
title: What can I do to prevent the "runtimeerror dictionary changed size during iteration" error?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-02 00:00:00
updated_at: 2023-02-02 00:00:00
tldr: Avoid modifying the dictionary while iterating over it.
---

**Contents**

[TOC]

# Section 1: Understanding the Error
The "RuntimeError: dictionary changed size during iteration" error occurs when a dictionary is modified while it is being iterated over. This is because the dictionary's size is changing while the code is trying to access elements in the dictionary, causing the code to fail.

# Section 2: Avoiding the Error
The best way to avoid this error is to not modify the dictionary while it is being iterated over. This can be done by either creating a copy of the dictionary and iterating over the copy, or by using a for loop to iterate over the dictionary instead of a while loop.

# Section 3: Alternative Solutions
If modifying the dictionary while iterating is necessary, then an alternative solution is to use a for-else loop. This loop will execute the else statement only if the loop has finished iterating over the dictionary without any modifications.

# Section 4: Conclusion
In conclusion, the "RuntimeError: dictionary changed size during iteration" error can be avoided by not modifying the dictionary while it is being iterated over, or by using a for-else loop if modifications are necessary.
