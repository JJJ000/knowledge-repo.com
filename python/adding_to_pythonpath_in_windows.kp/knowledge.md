---
title: What is the process for adding a module/package to the pythonpath in windows?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-02 00:00:00
updated_at: 2023-02-02 00:00:00
tldr: Add the directory containing the modules/packages to the PYTHONPATH environment variable.
---

**Contents**

[TOC]

1. **Setting the Environment Variable**

- Open the Control Panel.
- Go to System and Security > System > Advanced system settings.
- In the Advanced tab, click the Environment Variables button.
- Under System Variables, click New.
- Enter PYTHONPATH in the Variable Name field.
- Enter the path to the Python modules in the Variable Value field.
- Click OK.

2. **Verifying the Path**

- Open the Command Prompt.
- Type `echo %PYTHONPATH%` and press Enter.
- Verify that the path to the Python modules is displayed.

3. **Testing the Path**

- Open the Command Prompt.
- Change the directory to the location of the Python modules.
- Type `python` and press Enter.
- Verify that the Python interpreter is running.

4. **Adding to the Path**

- Open the Command Prompt.
- Type `set PYTHONPATH=%PYTHONPATH%;[path to modules]` and press Enter.
- Verify that the path to the Python modules is included in the PYTHONPATH environment variable.
