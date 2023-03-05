---
title: A step-by-step guide on how to uninstall Python anaconda without encountering any potential issues
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-05 00:00:00
updated_at: 2023-03-05 00:00:00
tldr: To safely uninstall Python Anaconda, you can delete the Anaconda folder from your system and remove it from your system`s PATH environment variable.
---

**Contents**

[TOC]

Uninstalling Python Anaconda

To uninstall Python Anaconda, follow the steps outlined below:

1. Removing Anaconda from your PATH

The first step is to remove Anaconda from your PATH (environment variable). Here's how: 

- Open the Anaconda Prompt (or your terminal).
- Type 

  ```
  conda install anaconda-clean
  ```
  
  and Press enter. 
  
- Once the installation is complete, type 

  ```
  anaconda-clean
  ```
  
  and hit enter.
  
- You will be prompted with a confirmation message about whether you want to remove all Anaconda related files. Press `"Y"` and hit enter. This will uninstall Anaconda and remove all associated files and directories.

2. Deleting the Anaconda Installation Directory

Once the Anaconda is removed from your PATH, proceed to delete the Anaconda installation directory. 

- Open the File Explorer, navigate to the folder where you installed Anaconda, and delete the entire folder. The default installation directory is usually`"C:\Users\<username>\Anaconda3"`. 

3. Removing Anaconda from the Windows Registry

 After removing the Anaconda installation directory, it's important to check and remove any Anaconda-related entries in the Windows Registry. 

- Press the Windows key + R to open the Run dialog box.
- Type "regedit" and hit enter.
- Navigate to the following key:

  ```
  HKEY_CURRENT_USER\Software
  ```

- Look for any entries named "Anaconda" or "Continuum Analytics" under this key and delete them.
- Repeat the same process for the following keys: 

  ```
  HKEY_LOCAL_MACHINE\SOFTWARE
  HKEY_LOCAL_MACHINE\SOFTWARE\WOW6432Node
  ```

- Restart your computer for changes to take effect.

4. Cleaning up Python Environment 

If you had installed packages outside of your conda environments, you will need to remove them separately using pip or other package managers. 

- Open the command prompt (or your terminal) and type 

  ```
  pip freeze
  ```
  
  and hit enter. 
 
 This will display a list of all packages installed in your Python. 
 
- Make a note of which packages you need to keep and which ones you don't. Next, type 

  ```
  pip uninstall <package-name>
  ```
  
  to remove the unwanted packages.
  
- Repeat this process for all packages you want to remove from your Python environment.

That's it! With these steps, you have successfully uninstalled Python Anaconda from your system.  Make sure to check your PATH and registry settings to make sure all traces of Anaconda are removed.
