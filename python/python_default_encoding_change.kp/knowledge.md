---
title: How can the default encoding of Python be altered?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-11 00:00:00
updated_at: 2023-03-11 00:00:00
tldr: You can change the default encoding of Python by adding the following line of code at the beginning of your script `# -*- coding encoding -*-` where `encoding` is the name of the desired encoding (e.g. utf-8, iso-8859-1).
---

**Contents**

[TOC]

# Introduction
Python represents text using Unicode encoding by default. However, on certain occasions, it may be desirable to use a different encoding. This could be because of compatibility or speed reasons. This guide aims to show you how to change the default encoding of Python.

# Identifying the Default Encoding
Before changing the default encoding, it’s crucial to identify which encoding Python is currently using. This can be done by running the following command in your Python interpreter:

```
import sys
sys.getdefaultencoding()
```

The command should output the following:

```
utf-8
```

# Changing Default Encoding
There are two ways to change the default encoding of Python. The first method involves changing the encoding at runtime. This can be done using the `sys.setdefaultencoding()` method.

```
import sys
sys.setdefaultencoding('iso-8859-1')
```

However, it’s important to note that using `sys.setdefaultencoding()` is not recommended. This is because the method does not exist in Python 3 and is considered unsafe. The second, more recommended method involves exporting an environment variable.

# Exporting environment variable
To set the default encoding to a different encoding, you can export an environment variable. You can do this by setting the `PYTHONIOENCODING` variable to the desired encoding. For example, to set the encoding to ISO-8859-1 run the following command:

```
export PYTHONIOENCODING=iso-8859-1
```

To avoid running this command every time, you can add it to your shell startup script. 

# Conclusion
In conclusion, we have demonstrated two methods to change the default encoding of Python. Changing the default encoding should only be done in exceptional cases, as the standard encoding provides smooth compatibility with most systems.
