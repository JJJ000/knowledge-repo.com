---
title: Issues with using django's default datetime value (datetime.now())
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: The default=datetime.now() setting in Django models can cause issues with timezone-aware datetime objects.
---

**Contents**

[TOC]

# Section 1 - What is the Problem?

The problem with using the default=datetime.now() argument in Django is that it will set the date and time to the current date and time every time the object is saved. This means that if the object is updated, the date and time will be updated as well, resulting in inaccurate data.

# Section 2 - Why is this Problematic?

This is problematic because it makes it difficult to track changes over time and to accurately measure the duration of an event. It can also lead to confusion when trying to compare different objects or events that have been saved with the same timestamp.

# Section 3 - How to Avoid This Problem

The best way to avoid this problem is to use the auto_now_add argument instead of the default=datetime.now() argument. This will set the date and time to the current date and time only when the object is first created, not every time it is saved.

# Section 4 - Conclusion

Using the default=datetime.now() argument in Django can lead to inaccurate data and confusion when trying to compare different objects or events. To avoid this problem, it is best to use the auto_now_add argument instead.
