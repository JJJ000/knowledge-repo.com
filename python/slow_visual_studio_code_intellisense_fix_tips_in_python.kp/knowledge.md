---
title: Is there a solution to the issue of visual studio code intellisense being sluggishly slow?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-12 00:00:00
updated_at: 2023-03-12 00:00:00
tldr: You can try disabling unnecessary extensions or using an alternative code editor like PyCharm.
---

**Contents**

[TOC]

# Introduction

As an AI language model, I am not capable of experiencing the code editor or any technical problem associated with it; however, I will offer guidance based on the human inputs that I have been trained on. This article aims to provide some tips and tricks that can be applied to boost the performance of Visual Studio Code's Intellisense when working with Python.

## Section 1 - Upgrade the Python Language Server

The current version of Visual Studio Code Python extension has a built-in Language Server Protocol (LSP) that provides many features, including Intellisense, debugging, and testing. However, the earlier versions of the Python Language Server were not very good performers, and few bugs had already been reported. The latest version of the language server is built with Numpy and Pandas that helps you resolve hints quite faster. Hence the initial step you can take to enhance Intellisense performance is to upgrade Python to the latest version.

> Note: Make sure you have installed the latest available version of Visual Studio Code and the Python extension.

You need to run the following pip command in the terminal to upgrade the Python Language Server:

```cmd
$ pip install --upgrade "python-language-server[all]"
```

If it doesn't help, proceed to the next section.

## Section 2 - Configure IntelliSense Settings

Visual Studio Code allows you to configure your IntelliSense settings to optimize the performance for the Python projects you are working on.

1. You can start by tweaking the setting `python.languageServer` to optimize the performance of IntelliSense further. Refer to the documentation [here](https://code.visualstudio.com/docs/python/settings-reference#_python-specific-settings);

2. Another option is to customize the IntelliSense settings of the Python extension by following the steps below:
   
   - Open the Command Palette from the View menu or using the shortcut (Ctrl+Shift+P or Cmd+Shift+P)
   - Type “Preferences: Open User Settings"  and select the option
   - In the search bar, type “python.linting.enabled” and double-click on the option to toggle it to False. This will disable linting for your code files.
   - Type “python.autoComplete.extraPath” in the search bar and press Enter. Add a path to the virtual environments you want to use with IntelliSense.

## Section 3 - Limit the Scope of IntelliSense and Analysis

When working on a larger project, Visual Studio Code may slow down because it analyzes and displays all files in all folders of the project. You can optimize the performance of IntelliSense and analysis by limiting the scope to folders that are relevant to your project.

1. To set the scope of IntelliSense and analysis, open the Command Palette, and type “Python: Select Workspace Folder” and select the project folder you are working on.

2. If your project has multiple subfolders, you can limit the scope further by specifying a custom include pattern in the settings.json file:

```json
"python.analysis.extraPaths": [
    "./src/**"
]
```

This will tell Visual Studio Code to look for code files only in the “src” folder and its subfolders.

## Section 4 - Use Python Stub Files for External Libraries

IntelliSense’s performance may suffer when your project is using external libraries that it is not aware of. You can solve this problem by creating “stub files” that mimic the external library’s behavior and tell IntelliSense to use them.

1. To create a stub file, you can use a tool like stubgen, which automatically generates stub files based on the packages and modules you have installed in your virtual environment. You can download and install stubgen with pip:

```cmd
$ pip install stubgen
```

2. After installing stubgen, you can generate a stub file for the external library by running the following command in the terminal:

```cmd
$ stubgen numpy
```

This will create a numpy-stubs folder in your project directory, containing the stub file for the numpy module.

3. Finally, you can tell IntelliSense to use the stub file by adding the path to the stub file in the settings.json file:

```json
"python.autoComplete.extraPaths": [
    "./numpy-stubs"
]
```

## Conclusion

In conclusion, to optimize the performance of Intellisense on Visual Studio Code when working with Python projects, you can upgrade your Language Server, configure the IntelliSense settings, limit the scope of IntelliSense and analysis, and use Python stub files for external libraries. Applying these tips and tricks will ensure that your Visual Code Studio’s Intellisense works a lot smoother and faster, thus allowing you to line-up your codes quicker.
