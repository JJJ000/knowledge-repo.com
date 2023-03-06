---
title: While installing eventlet, the command 'gcc' terminated with an exit status of 1 due to an error
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: The error occurred because GCC compiler is not installed or not properly configured on the system.
---

**Contents**

[TOC]

Section 1: Introduction
When installing eventlet in Python, sometimes an error may occur showing that the command 'gcc' failed with exit status 1. This error can be frustrating as it prevents the successful installation of the eventlet package. This guide provides steps you can take to fix the error and ensure the installation of eventlet is successful.

Section 2: Install Required Dependencies
The error usually occurs when some dependencies required for eventlet are not installed or outdated. To fix this, you need to check the dependencies and update them. To install the required dependencies, you can use the following command:

```
sudo apt-get install build-essential python-dev
```

This command installs the required dependencies including build-essential and python-dev.

Section 3: Upgrade PIP
The error can also occur due to pip being outdated. To ensure your pip is up to date, run the following command:

```
pip install --upgrade pip
```

This command updates pip to the latest version. Once pip is updated, try to install eventlet again.

Section 4: Install Eventlet via PIP
After ensuring that the required dependencies are installed and pip is up to date, you can now install eventlet via pip. Use the following command to install eventlet:

```
pip install eventlet
```

This command installs eventlet and all the required packages. With these steps, the installation of eventlet should be successful without the error.
