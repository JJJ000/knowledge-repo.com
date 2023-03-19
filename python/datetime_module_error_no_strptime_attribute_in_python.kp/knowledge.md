---
title: The 'strptime' attribute is not present in the 'datetime' module, resulting in an attributeerror
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: The error occurs when trying to use the strptime method from the datetime module without importing it first.
---

**Contents**

[TOC]

Section 1: Understanding the error message

The error message, "AttributeError: 'datetime' module has no attribute 'strptime'" means that the python interpreter is not able to find the 'strptime' method in the 'datetime' module. This error occurs when a module is imported, but the attribute or method that is being called is not present in the module.

Section 2: Reasons for the error

There could be several reasons why this error occurs. Some of the reasons are:

1. Misspelling: One of the most common reasons for this error is misspelling. For example, if you spell 'strptime' as 'strtpime', the interpreter won't be able to find it in the 'datetime' module.

2. Importing the wrong module: If you import a module that does not have the 'strptime' method, you will get this error. For example, if you import the 'time' module instead of the 'datetime' module, you will get this error.

3. Python version: The 'strptime' method was introduced in Python 2.4. If you are using an older version of Python, you will get this error.

Section 3: Solutions to fix the error

To fix the "AttributeError: 'datetime' module has no attribute 'strptime'" error, you can try the following solutions:

1. Check the spelling: Make sure that you have spelled 'strptime' correctly. If you have misspelled it, correct the spelling.

2. Import the right module: Make sure that you have imported the 'datetime' module and not any other module like 'time' or 'dateutil'. If you have imported the wrong module, correct the import statement.

3. Upgrade your Python version: If you are using an older version of Python, upgrade to a newer version that has the 'strptime' method.

Section 4: Example code

Here is an example code that throws the "AttributeError: 'datetime' module has no attribute 'strptime'" error:

```
import datetime

date_string = '2022-10-30'
date_obj = datetime.strptime(date_string, '%Y-%m-%d')
print(date_obj)
```

To fix this error, we need to replace the line `date_obj = datetime.strptime(date_string, '%Y-%m-%d')` with the correct code: `date_obj = datetime.datetime.strptime(date_string, '%Y-%m-%d')`. This is because the 'strptime' method is present in the 'datetime' class of the 'datetime' module. Here is the corrected code:

```
import datetime

date_string = '2022-10-30'
date_obj = datetime.datetime.strptime(date_string, '%Y-%m-%d')
print(date_obj)
``` 

The output will be: `2022-10-30 00:00:00`.
