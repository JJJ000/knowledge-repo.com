---
title: What is the method to specify the working directory for Python program debugging in vscode?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: In VSCode, set the `cwd` (current working directory) property in your launch.json configuration file to the desired directory.
---

**Contents**

[TOC]

## Section 1: Introduction

Visual Studio Code is a popular code editor that is widely used by developers. It comes with many features that help developers to write, debug and test their programs quickly and efficiently. One of the essential features is the ability to debug code in the editor. In this tutorial, we will learn how to set the working directory for debugging a python program in Visual Studio Code.

## Section 2: Setting the working directory

By default, Visual Studio Code will use the current directory of the Python program as the working directory when debugging. However, you can change the working directory to a different directory by following these steps:

1. Open your Python program in Visual Studio Code
2. On the left-hand side of the screen, click the 'Run and Debug' button (or use the shortcut keys Ctrl+Shift+D).
3. Click the gear icon in the top right corner of the Run and Debug panel and select 'Open Configurations'
4. In the 'launch.json' file, find the configuration for your Python program.
5. Add the 'cwd' property to your configuration and set its value to the path of the directory you want to use as the working directory.

Here is an example of how to set the working directory for a Python program using the launch.json file:

```json
{
    "version": "0.2.0",
    "configurations": [
        {
            "name": "Python: Current File (Integrated Terminal)",
            "type": "python",
            "request": "launch",
            "program": "${file}",
            "cwd": "${workspaceFolder}/src"
        }
    ]
}
```

In this example, we set the working directory to the 'src' folder of the project using the "${workspaceFolder}" variable. 

## Section 3: Using relative paths

You can also use relative paths to set the working directory for your Python program. This is useful when you want to set the working directory to a subdirectory of the current directory.

For example, to set the working directory to a subdirectory named 'data', you can use the following configuration:

```json
{
    "version": "0.2.0",
    "configurations": [
        {
            "name": "Python: Current File (Integrated Terminal)",
            "type": "python",
            "request": "launch",
            "program": "${file}",
            "cwd": "${fileDirname}/data"
        }
    ]
}
```

In this example, we set the working directory to a subdirectory named 'data' using the "${fileDirname}" variable, which represents the directory of the current file.

## Section 4: Conclusion

In this tutorial, we learned how to set the working directory for debugging a Python program in Visual Studio Code. By changing the working directory, we can access files and resources from different locations, making it easier to test and debug our code. Keep in mind that setting the working directory is just one of the many ways to improve your Python programming experience in Visual Studio Code.
