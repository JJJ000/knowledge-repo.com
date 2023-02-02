---
title: What is the process for removing Python 2.7 from a mac os x 10.6.4 system?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-02 00:00:00
updated_at: 2023-02-02 00:00:00
tldr: Run the uninstaller located in the `Python 2.7` folder in the Applications folder.
---

**Contents**

[TOC]

## Uninstalling Python 2.7
1. Open Finder and navigate to the Applications folder.
2. Find the Python 2.7 folder and drag it to the Trash.
3. Empty the Trash.

## Removing Python 2.7 Files
1. Open the Terminal application (in the Utilities folder).
2. Type the following command: `sudo rm -rf /Library/Frameworks/Python.framework`
3. Enter your password when prompted.
4. Type `y` to confirm the deletion.
5. Type `sudo rm -rf /usr/bin/python`
6. Type `y` to confirm the deletion.
7. Quit the Terminal application.
