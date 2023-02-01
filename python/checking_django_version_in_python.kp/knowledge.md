---
title: What is the version of django?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-01 00:00:00
updated_at: 2023-02-01 00:00:00
tldr: The Django version can be checked by using the django.VERSION attribute in Python.
---

**Contents**

[TOC]

# Check Django Version

## Using Command Line

The easiest way to check the version of Django is to use the command line.

1. Open the command line.
2. Type `python -m django --version` and press enter.

The output will be the Django version.

## Using Python Script

You can also check the Django version using a Python script.

1. Create a new Python file in your favorite text editor.
2. Add the following code to the file:

```python
import django
print(django.get_version())
```

3. Save the file and run it.

The output will be the Django version.
