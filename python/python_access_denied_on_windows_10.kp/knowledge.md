---
title: I am unable to run Python on windows 10 due to a "permission denied" error
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-07 00:00:00
updated_at: 2023-03-07 00:00:00
tldr: Try running the program as an administrator.
---

**Contents**

[TOC]

# Introduction
Python is a popular programming language that can run on different operating systems, including Windows 10. However, sometimes when attempting to run it, an error message may occur, stating "Permission Denied." This error usually prevents users from executing their Python script. 

There are several reasons for the permission denied error to occur. The most common causes are related to user permission settings or folder/file access control.

In this article, we will walk you through some possible solutions to resolve this issue and allow you to run Python scripts on Windows 10 without permission-related problems.

## 1. Run as administrator 

The first solution you can try when receiving the permission denied error when launching Python is to run it as an administrator. Running programs as administer is necessary when the program needs to make changes to the system or files that require elevated rights.

The steps to execute a command prompt window as an administrator are:

Step 1: Click on the start menu
Step 2: Type cmd
Step 3: Right-click on Command Prompt and select "Run as administrator."

If you prefer to execute Python from the command prompt, ensure to execute the cmd prompt as administrator.

## 2. Granting folder/file permissions 

Sometimes, permission denied errors concerning Python can be caused by the user's lack of access rights to edit, create, or delete files and folders on the computer.

In such a situation, granting the user permission to access the folder or file should resolve the permission denied issue. 

How to grant permissions:

Step 1: Navigate to the file or folder having permission issues.
Step 2: Right-click on the file/folder
Step 3: Select "Properties."
Step 4: Go to the "Security" tab.
Step 5: Click on "Edit."
Step 6: Add the user that you want to give access to the file/folder.
Step 7: Check the box associated with the appropriate level of access.

## 3. Edit Security Policies 

For organizations that set the security policies to Limited features, it might not allow Python to run correctly.

The solution is editing the security policies to allow Python to run. The steps to follow are:

Step 1: Press the Windows key + R.
Step 2: Type gpedit.msc.
Step 3: Select Computer Configuration.
Step 4: Go to Windows Settings.
Step 5: Click Security Settings.
Step 6: Select the Local Policies.
Step 7: Click on Security options.
Step 8: Search for the “User Account Control: Run all administrators in Admin approval mode” policy.
Step 9: Change its settings to "Disabled."
Step 10: Save the changes.

## 4. Disable Windows Defender 

Sometimes, Windows Defender, the built-in antivirus software in Windows 10, can block the installation of the Python runtime, causing the permission denied error message.

To disable Windows Defender and allow Python to run:

Step 1: Click on the Start menu.
Step 2: Search for "Windows Security" and select "Open Windows Security."
Step 3: Click on "Virus & threat protection."
Step 4: Click on "Manage settings" under "Virus & threat protection settings."
Step 5: Turn off Real-time protection.

Conclusion:
In conclusion, the error message, "Permission Denied" in Windows 10 while attempting to run Python, can be caused by various issues. However, the solutions listed above will help you resolve the problem and allow you to run Python scripts without any issues.
