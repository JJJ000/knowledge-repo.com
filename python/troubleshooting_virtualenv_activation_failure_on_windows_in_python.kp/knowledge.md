---
title: On windows, it is not possible to activate 'virtualenv'
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-16 00:00:00
updated_at: 2023-03-16 00:00:00
tldr: Try running the command `Scripts/activate` instead of `activate.bat` in the command prompt in order to activate virtualenv on Windows in Python.
---

**Contents**

[TOC]

## Possible Reasons

- Virtual environment is not properly installed.
- The path to the virtual environment is incorrect.
- There is a conflict with the version of Python being used.
- The virtual environment is not properly activated.


## Solutions

1. Make sure virtual environment is properly installed:

   Use the pip installer to install virtualenv with the following command in the terminal:

   ```
   pip install virtualenv
   ```

2. Check the path to the virtual environment:

   Make sure you have navigated to the correct directory containing the virtual environment. To activate the environment, use the following command:

   ```
   .\venv\Scripts\activate
   ```

3. Check for Python version conflicts:

   Make sure that you have installed a compatible version of Python on your machine. Confirm the version of Python installed using the following command:

   ```
   python --version
   ```

   If the version is not compatible with the virtual environment, create a new environment or update the version of Python.

4. Check if the virtual environment is properly activated:

   After running the activation command, the virtual environment name should appear on the terminal prompt. If it does not appear, the environment is not properly activated. Try running the command to activate the environment again.

   ```
   .\venv\Scripts\activate
   ```


## Conclusion

Make sure virtualenv is properly installed, the path to the environment is correct, and the environment is properly activated. Check for any version conflicts and update your environment or Python version if necessary.
