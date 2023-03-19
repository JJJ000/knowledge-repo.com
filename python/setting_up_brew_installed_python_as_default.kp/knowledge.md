---
title: Can you guide me on how to make Python installed via brew the default python?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: Add the following line to your shell configuration file (.bashrc or .zshrc) `export PATH=/usr/local/opt/python/libexec/bin$PATH`.
---

**Contents**

[TOC]

## Checking the current version of Python on your system

Before switching your default Python version to the one installed using Homebrew, verify which version of Python is currently being used on your system. This can be done by opening Terminal and entering the following command:

```
python --version
```

This will display the current version of Python installed on the system.


## Updating the PATH environment variable

In order to make the newly installed Python through Homebrew the default version, you need to update the PATH environment variable. This tells the system where to find the executable files for Python. To update the PATH environment variable, follow these steps:

1. Open Terminal
2. Enter the following command to open the .bash_profile file:

    ```
    nano ~/.bash_profile
    ```

3. Add the following line at the end of the file:

    ```
    export PATH=/usr/local/opt/python/libexec/bin:$PATH
    ```

4. Save and exit by pressing `CTRL`+`X`, then pressing `Y` to save changes.

5. Restart Terminal, or enter the following command for the changes to take effect:

    ```
    source ~/.bash_profile
    ```

## Verifying that the default Python has been updated

After updating the PATH environment variable, verify that the default version of Python has been updated by entering the following command:

```
python --version
```

This should display the version of Python installed via Homebrew, indicating that it is now the default version. 

If the command output still shows the old Python version, check that the PATH variable was updated correctly by entering the following command:

```
echo $PATH
```

This should display the updated PATH variable with the location of the new Python installation directory listed.
