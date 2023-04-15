---
title: Modify the setting to skip verification prompt while executing pip uninstall
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Use the -y or --yes flag to bypass the confirmation prompt for pip uninstall in Python.
---

**Contents**

[TOC]

## The Prompt

When uninstalling a package using pip in Python, a confirmation prompt appears to confirm whether the user wants to proceed with the uninstallation. The prompt looks like this:

```
Uninstall XYZ (y/N)
```

where `XYZ` is the name of the package being uninstalled.

## Bypassing the Prompt with the -y Flag

The prompt can be bypassed by using the `-y` flag with the `pip uninstall` command. This flag automatically answers "yes" to the prompt, effectively bypassing it. The command looks like this:

```
pip uninstall XYZ -y
```

where `XYZ` is the name of the package being uninstalled. By using the `-y` flag, the package will be uninstalled without any confirmation prompt.

## Disabling the Prompt Globally

If you frequently uninstall packages using pip and want to permanently disable the confirmation prompt, you can edit your `pip.conf` file to include the following line:

```
uninstall = -y
```

This line tells pip to always use the `-y` flag when uninstalling packages and therefore bypass the confirmation prompt. 

The `pip.conf` file can be found in different locations depending on the operating system and the installation method used for Python. On Linux and macOS, it is usually located at `~/.config/pip/pip.conf`, while on Windows it can be found at `%APPDATA%\pip\pip.ini`.

## Bypassing the Prompt in a Script

If you want to uninstall a package without being prompted for confirmation in a Python script, you can use the `subprocess` module to run the `pip` command with the `-y` flag. Here's an example:

```python
import subprocess

package_name = 'XYZ'
subprocess.call(['pip', 'uninstall', package_name, '-y'])
```

This script will uninstall the package named `XYZ` without any confirmation prompt. 

Note that using the `-y` flag in a script can be dangerous if the package being uninstalled has dependencies that will also be removed. In such cases, it's better to prompt the user for confirmation before proceeding with the uninstallation.
