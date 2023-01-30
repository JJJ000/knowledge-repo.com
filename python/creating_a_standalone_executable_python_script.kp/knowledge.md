---
title: What is the best way to create a Python script that can be run independently, with no external dependencies?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-01-30 00:00:00
updated_at: 2023-01-30 00:00:00
tldr: You can use a tool such as PyInstaller to create a standalone executable from a Python script that will run without any dependencies.
---

**Contents**

[TOC]

**Section 1: Compiling the Script**

In order to make a Python script standalone executable, it must first be compiled. This can be done using a variety of tools, such as py2exe, pyinstaller, and cx_Freeze. Each of these tools will take the Python script and compile it into an executable file that can be run without any other dependencies.

**Section 2: Packaging Dependencies**

Once the script has been compiled, any necessary dependencies must be packaged with the executable file. This can be done using the same tools used to compile the script, but they will need to be configured to include the necessary libraries and modules. Once the dependencies have been packaged, the executable file can be run without any additional dependencies.

**Section 3: Testing the Executable**

Once the executable file has been created, it should be tested to ensure that it runs correctly and without any errors. This can be done by running the executable on a clean system and ensuring that it works as expected.

**Section 4: Distributing the Executable**

The final step is to distribute the executable file. This can be done by placing the executable on a web server or by sending it out via email. Once the executable has been distributed, users can run it without any additional dependencies.
