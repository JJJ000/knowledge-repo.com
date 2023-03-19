---
title: How to debug a Python script with parameters using visual studio code
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-07 00:00:00
updated_at: 2023-03-07 00:00:00
tldr: In Visual Studio Code, you can debug a Python script with arguments by setting the `args` attribute in the launch configuration.
---

**Contents**

[TOC]

# Setting Up Debug Configuration in Visual Studio Code
1. Open your Python script in Visual Studio Code.
2. Click on the Debug icon on the left-hand menu bar or press Ctrl+Shift+D on your keyboard.
3. Click on the gear icon or `Add Configuration` button to open the launch.json file.
4. Add a new configuration of type `Python` by clicking on the `+` icon in the top right corner.
5. Give a name to the configuration and set the `program` field to the path of your Python script.
6. Set the `args` field to the arguments you want to pass to your Python script.

# Running the Debugger with Arguments
1. Click on the Run icon on the left-hand menu bar or press Ctrl+Shift+D on your keyboard.
2. Select the debug configuration that you have setup earlier and click on `Run` button.
3. The debugger will start with the arguments passed to your Python script.
4. You can set breakpoints in your Python script and step through the code to debug it.

# Tips and Tricks
- Use the `console.log` function to output debugging information to the console.
- Use the `Debug Console` tab to interact with your Python script during debugging.
- Use the `Watch` tab to monitor variables and expressions during debugging.
- Use the `Ctrl+Shift+F5` shortcut to restart the debugger with the same configuration and parameters as the previous debug session.
