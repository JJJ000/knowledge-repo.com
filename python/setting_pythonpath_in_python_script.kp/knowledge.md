---
title: How can I configure pythonpath in a Python script?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-13 00:00:00
updated_at: 2023-03-13 00:00:00
tldr: You can set the PYTHONPATH environment variable to specify additional directories where Python should look for modules and packages.
---

**Contents**

[TOC]

# Setting PYTHONPATH in Python

## Method 1: Using the Command Prompt (Windows)

1. Open the Command Prompt and navigate to the directory where your Python scripts are saved.
2. Set the PYTHONPATH variable with the following command: 

   ```
   set PYTHONPATH=C:\path\to\directory\
   ```
   Make sure to replace 'C:\path\to\directory\' with the actual path to the directory where your Python scripts are saved.

3. You can now run your Python scripts from the Command Prompt, and Python will look for any import statements in the specified directory.

## Method 2: Using the os Module (Cross-platform)

1. Import the os module at the beginning of your Python script: 

   ```
   import os
   ```

2. Set the PYTHONPATH variable using the following code: 

   ```
   os.environ['PYTHONPATH'] = '/path/to/directory'
   ```
   Make sure to replace '/path/to/directory' with the actual path to the directory where your Python scripts are saved.

3. You can now run your Python scripts, and Python will look for any import statements in the specified directory.


## Method 3: Setting PYTHONPATH permanently

1. Open the System Properties window (Windows) or the Terminal (Linux)
2. Click on "Advanced system settings" (Windows) or run ```sudo nano /etc/environment``` (Linux)
3. Click on "Environment Variables" (Windows) or add the following line at the end of the file ```export PYTHONPATH="/path/to/directory"``` (Linux)
4. Save changes and exit the window / file
5. Restart your computer / terminal for changes to take effect

Now you will be able to use the imported modules from directory specified in "PYTHONPATH" environment variable.
