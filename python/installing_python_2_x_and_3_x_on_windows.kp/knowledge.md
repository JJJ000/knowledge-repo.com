---
title: What is the process for installing both Python 2.x and Python 3.x on windows?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: Download and install Python 2.x and Python 3.x separately from their official websites and remember to set the environment variables accordingly for both versions.
---

**Contents**

[TOC]

## Installing Python 2.x

1. Download Python 2.x installer from the official website (https://www.python.org/downloads/release/python-2718/)
2. Run the installer and select 'Customize installation'
3. Choose the directory where you want to install Python 2.x.
4. Select the components you wish to install, such as pip, documentation, and IDLE.
5. Complete the installation process.



## Installing Python 3.x

1. Download Python 3.x installer from the official website (https://www.python.org/downloads/release/python-381/)
2. Run the installer and select 'Customize installation'
3. Choose the directory where you want to install Python 3.x.
4. Select the components you wish to install, such as pip, documentation, and IDLE.
5. Complete the installation process.


## Configuring the system PATH environment variable

1. Open the Start menu and search for "Environment Variables".
2. Click on "Edit the system environment variables".
3. Click on the "Environment Variables" button.
4. Under "System variables", scroll down and find the "Path" variable, then click on "Edit".
5. Add the Python installation paths to the PATH variable. For example, if you installed Python 2.x in `C:\Python27` and Python 3.x in `C:\Python38`, add `C:\Python27` and `C:\Python38` to the PATH variable, separating them with a semicolon.
6. Click "OK" to save the changes and close all the windows.


## Verifying the installation

1. Open Command Prompt window by pressing Win + R and typing cmd in the Run dialog box.
2. Type "python2" (without quotes) to start Python 2.x.
3. Type "python3" (without quotes) to start Python 3.x.
4. Verify that the Python versions you installed are running correctly by entering some basic commands like `print("Hello, World!")` in each version.
