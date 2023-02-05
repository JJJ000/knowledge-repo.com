---
title: The 'chromedriver' program must be in your system's directory for it to be used
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: The chromedriver executable needs to be added to the PATH environment variable.
---

**Contents**

[TOC]

# Solution

## Explanation
This error occurs when the ChromeDriver executable is not available in the system's PATH environment variable. ChromeDriver is a web driver used to control the Chrome browser from a program, such as a Python script. It is necessary for running automated tests on webpages.

## Resolution
1. Download the ChromeDriver executable from the [ChromeDriver downloads page](https://chromedriver.chromium.org/downloads).
2. Extract the executable file from the downloaded archive.
3. Add the path of the extracted executable to the PATH environment variable.
4. Restart the system or the terminal window to apply the changes.
