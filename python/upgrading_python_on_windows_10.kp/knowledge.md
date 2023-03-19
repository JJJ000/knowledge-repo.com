---
title: In windows 10, what is the procedure for upgrading the Python installation?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-07 00:00:00
updated_at: 2023-03-07 00:00:00
tldr: To upgrade the Python installation in Windows 10, download the latest version of Python from the official website and install it over the existing installation.
---

**Contents**

[TOC]

## Checking the Current Version of Python

Before upgrading Python, it is important to know the version that is currently installed on your Windows 10 computer. To check the current version of Python, follow these steps:

1. Open the command prompt by pressing the Windows key + R and typing "cmd" in the run dialog box.

2. In the command prompt window, type "python -V" (without the quotes) and press enter.

3. The version number of the currently installed Python will be displayed. 


## Downloading and Installing the Latest Python Version

To upgrade Python, the latest version must be downloaded from the official Python website and installed on your computer. Follow these steps:

1. Go to the official website (https://www.python.org/downloads/) and download the latest version according to your system's architecture and the required configuration.

2. Once downloaded, run the installer file and select the "Add Python X.X to PATH" option during the installation process.

3. Follow the on-screen instructions and complete the installation process.


## Adding Python to the System Path

When installing Python, it is important to add it to the system path so that it can be accessed from any location in the system. Here's how to do it:

1. In the Windows search bar, type "env" and select "Edit the system environment variables".

2. Click on the "Environment Variables" button.

3. Under "System Variables", scroll down to "Path" and select it.

4. Click on the "Edit" button and then "New".

5. Type in the path of the Python installation directory, for example, "C:\PythonXX" (without the quotes). Replace "XX" with the version number of Python installed.

6. Click "OK" on all windows to save changes.


## Verifying the Installation

To verify that the new version of Python is installed correctly, follow these steps:

1. Open the command prompt.

2. Type "python -V" (without the quotes) and press enter.

3. The version number of the newly installed Python will be displayed.

4. You can also open the Python IDLE by typing "python" in the command prompt, then check its version by typing "import sys; print(sys.version)" (without the quotes).
