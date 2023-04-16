---
title: Error the requests module could not be found
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: The requests module needs to be installed in order to use it in Python.
---

**Contents**

[TOC]

# Installation

The `requests` module is not part of the standard Python library and must be installed separately. The recommended way to install `requests` is to use the `pip` package manager. To install `requests` using `pip`, open a terminal window and type:

```
pip install requests
```

# Verifying Installation

Once `requests` is installed, you can verify the installation by opening a Python interpreter and typing:

```
import requests
```

If the module is installed correctly, you should see no errors.

# Troubleshooting

If you encounter an error when trying to import `requests`, it may be due to a conflict between different versions of Python or a missing dependency. Try running the following command to ensure all dependencies are installed:

```
pip install -r requirements.txt
```

If the problem persists, consider uninstalling and reinstalling the `requests` module.
