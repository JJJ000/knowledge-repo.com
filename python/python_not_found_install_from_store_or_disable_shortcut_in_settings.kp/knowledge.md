---
title: If Python is not detected, you can install it from the microsoft store by running the program without any arguments. alternatively, you may disable this shortcut from settings
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-13 00:00:00
updated_at: 2023-03-13 00:00:00
tldr: The error message suggests that Python is not installed on the system and provides options to install it from the Microsoft Store or disable the shortcut.
---

**Contents**

[TOC]

Possible answer:

# Problem description

When trying to run Python on a Windows computer, the user may encounter the following error message:

```
Python was not found; run without arguments to install from the Microsoft Store,
or disable this shortcut from Settings
```

This message indicates that Python is not installed on the system, or that the system cannot find the Python executable even though it is installed. This can happen for various reasons, such as a missing or incorrect PATH environment variable, conflicting Python installations, or incomplete installation or uninstallation of Python or related programs.

To solve this problem, the user can try one or more of the following solutions.

# Solution 1: Check PATH environment variable

One possible reason for the error message is that Python is not in the system's PATH environment variable, which is a list of directories where the system looks for executable files. To check and modify the PATH variable, follow these steps:

1. Open the Control Panel and go to System and Security -> System -> Advanced system settings -> Environment Variables.
2. In the System Variables section, scroll down to the Path variable and click Edit.
3. Check if the path to the Python executable directory is included in the list. If not, click New and add the path to the directory, such as "C:\Python39" for Python 3.9. Make sure to separate the paths with semicolons (;).
4. Click OK and close all the windows. Try running Python again.

If the PATH variable is correct, or if this solution does not work, try the next one.

# Solution 2: Reinstall Python

Another possible reason for the error message is that the Python installation is corrupted or incomplete. To reinstall Python, follow these steps:

1. Uninstall any existing Python installations from the Control Panel -> Programs and Features or by running the uninstaller from the installation directory.
2. Download the latest version of Python from the official website (https://www.python.org/downloads/windows/) and run the installer.
3. Choose the default settings or customize them as needed, but make sure to enable the "Add to PATH" option.
4. Finish the installation and try running Python again.

If the reinstallation does not work, or if the user has multiple versions of Python installed, try the next solution.

# Solution 3: Use a virtual environment

Sometimes, the system may confuse different Python versions or installations, causing the error message to appear. One way to avoid this issue is to use a virtual environment, which is a self-contained Python installation that can be isolated from the system's Python.

To create and activate a virtual environment, follow these steps:

1. Open a command prompt or PowerShell window and navigate to the desired directory where the virtual environment will be created (e.g., "cd C:\Users\user\Documents").
2. Run the command "python -m venv venv" to create a new virtual environment named "venv" (or any other name).
3. Activate the virtual environment by running the command "venv\Scripts\activate" (Windows) or "source venv/bin/activate" (Unix/Mac).
4. The command prompt should now show the virtual environment name in parentheses, indicating that any Python packages or scripts installed or run from now on will use the virtual environment's Python version and dependencies.
5. Install any packages or run any scripts as usual, but make sure to do it in the activated virtual environment.

If the virtual environment still cannot find Python, or if the user prefers not to use virtual environments, try the last solution.

# Solution 4: Disable the Python shortcut

Finally, if none of the above solutions work, the user can try disabling the Python shortcut that triggers the error message. To do this, follow these steps:

1. Right-click on the Python shortcut on the desktop or Start menu and select Properties.
2. In the Target field, add the parameter "-x" at the end of the command, without the quotes, so that it reads something like "C:\Python39\python.exe -x".
3. Click OK and try running Python again from the command prompt or PowerShell window.
4. If the problem persists or if the icon disappears, try either reinstalling Python or creating a new shortcut from the installation directory.

By following these solutions, the user should be able to resolve the Python not found error and start using Python on their Windows machine.
