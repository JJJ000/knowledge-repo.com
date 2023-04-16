---
title: Suppress tensorflow debugging output
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Set the environment variable TF\_CPP\_MIN\_LOG\_LEVEL to `3`.
---

**Contents**

[TOC]

# Section 1: Overview

Tensorflow is an open source software library for machine learning. It is used for numerical computation and large-scale machine learning. Debugging information can be disabled in Tensorflow in Python by setting the environment variable TF_CPP_MIN_LOG_LEVEL to 3.

# Section 2: Setting the Environment Variable

The environment variable TF_CPP_MIN_LOG_LEVEL needs to be set to 3 in order to disable Tensorflow debugging information in Python. This can be done by using the os.environ.setdefault() method. The following example shows how to set the environment variable:

```python
import os
os.environ.setdefault('TF_CPP_MIN_LOG_LEVEL', '3')
```

# Section 3: Values for the Environment Variable

The environment variable TF_CPP_MIN_LOG_LEVEL can be set to one of the following values:

* 0: Debug log messages are printed.
* 1: Informational log messages are printed.
* 2: Warning log messages are printed.
* 3: Error log messages are printed.

Setting the environment variable to 3 will disable all debug, informational, and warning log messages.

# Section 4: Conclusion

In conclusion, Tensorflow debugging information can be disabled in Python by setting the environment variable TF_CPP_MIN_LOG_LEVEL to 3. This can be done by using the os.environ.setdefault() method. The environment variable can be set to one of the following values: 0, 1, 2, or 3. Setting the environment variable to 3 will disable all debug, informational, and warning log messages.
