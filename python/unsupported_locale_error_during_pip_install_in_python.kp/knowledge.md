---
title: The error "unsupported locale setting" occurred while trying to execute the command "pip install"
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: The error occurs when the Python interpreter encounters an unsupported locale setting during installation of a package using pip.
---

**Contents**

[TOC]

Section 1: Introduction
When you try to install a Python package using pip, you might come across the following error: "locale.Error: unsupported locale setting". This error occurs when your system language settings do not match the recommended format. In this guide, we will explain how you can solve this issue.

Section 2: Verify Your System Language Settings
To check your system language settings, open a terminal window and enter the following command:
```
locale -a
```
This command will display a list of all available locales on your system. Look for the recommended locale settings that match your language and country.

Section 3: Set Your Locale Environment Variables
If you find the recommended locale settings in the previous step, you can set the appropriate environment variables. For example, if the recommended locale is 'en_US.UTF-8', you can set the environment variables by running the following commands:
```
export LC_ALL=en_US.UTF-8
export LANG=en_US.UTF-8
```
After setting these variables, try running the 'pip install' command again, and the unsupported locale setting error should be resolved.

Section 4: Conclusion
The "locale.Error: unsupported locale setting" error can be fixed by verifying your system language settings and setting the appropriate environment variables. By following the steps outlined in this guide, you should now be able to install Python packages using pip without any issues.
