---
title: What is the proper way to fully remove anaconda from macos?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-07 00:00:00
updated_at: 2023-03-07 00:00:00
tldr: To uninstall Anaconda completely from macOS in Python, run the following command in the terminal 

```bash
rm -rf ~/anaconda3
```
---

**Contents**

[TOC]

## Uninstalling Anaconda on macOS

If you need to completely uninstall Anaconda on macOS, you can follow these steps:

### Step 1: Remove the Anaconda files
- Open the Terminal app (Applications > Utilities > Terminal).
- Type `rm -rf ~/anaconda3` and press Enter to remove the main Anaconda directory. This will delete the entire directory and all its contents.
- Type `nano ~/.bash_profile` and press Enter to open the bash profile in the Terminal editor.
- Remove any Anaconda-related lines that were added to the file, such as `export PATH="/Users/your-username/anaconda3/bin:$PATH"`.
- Press `ctrl + x`, then `y`, and then `Enter` to save the changes and exit the editor.

### Step 2: Remove the Anaconda Launcher
- Open the Finder app and navigate to the "Applications" folder.
- Drag the "Anaconda-Navigator" icon to the trash can to remove the Anaconda Launcher application.

### Step 3: Remove the Anaconda data
- Open the Finder app and navigate to your user folder (the one with your username).
- Delete the `.anaconda` folder to remove any remaining Anaconda configuration data.

### Step 4: Verify the uninstallation
- Open the Terminal app and type `conda --version`. If Anaconda is no longer installed, you should see a message that says "conda: command not found".

## Conclusion
By following these steps, you should be able to successfully remove Anaconda from your macOS system. Make sure to double-check and verify that all Anaconda files and data have been removed to prevent any potential issues or conflicts with future software installations.
