---
title: When I type 'python', the windows store is launched by cmd
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-05 00:00:00
updated_at: 2023-03-05 00:00:00
tldr: This may be because the `python` command is not recognized by your computer and is interpreted as a search term by the Windows operating system, leading to a default search action in the Windows Store.
---

**Contents**

[TOC]

Possible solution:

## Check the PATH environment variable

The first thing to check is whether the location of the Python executable is properly included in the system's PATH environment variable. To do this:

1. Press Win+R to open the Run dialog box.
2. Type "sysdm.cpl" and press Enter to open the System Properties window.
3. Click on the "Advanced" tab and then click on the "Environment Variables" button.
4. Under "System Variables", locate the "Path" entry and click on "Edit".
5. Make sure that the directory containing the "python.exe" file (e.g., "C:\Python39") is included in the list of directories separated by semicolons.
6. Click "OK" on all open windows to save the changes.
7. Open a new instance of CMD and try to run "python" again.

## Check the file associations

Another possible cause for CMD opening the Windows Store instead of Python could be a misconfigured file association. To check and fix this:

1. In the CMD window, type "assoc .py" and press Enter.
2. The output should be ".py=Python.File", which means that Python should be the default program to open Python scripts.
3. If the output is different or missing, type "ftype Python.File=C:\Path\to\python.exe \"%1\" %*" (replace "C:\Path\to\python.exe" with the actual path to the Python executable) and press Enter.
4. Try to run "python" again and see if it works.

## Check for malware or unwanted software

If the above solutions don't solve the issue, it's possible that malware or unwanted software is interfering with the CMD command. To check and remove any such program:

1. Scan the system with a reputable anti-malware or anti-virus software to detect and quarantine any threats.
2. Use the Windows Task Manager to identify any suspicious processes running in the background, especially those that start with "ms" or "store".
3. Uninstall any recently installed programs or updates that might have caused the problem.
4. Reset the Windows Store cache by running "wsreset.exe" in CMD (make sure to run it as administrator).
5. Try to run "python" again and see if the problem persists.
