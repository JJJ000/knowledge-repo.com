---
title: In interactive python, what is the method to view the complete command history?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-07 00:00:00
updated_at: 2023-03-07 00:00:00
tldr: Type `history` or `hist` in the interactive Python shell to see the entire command history.
---

**Contents**

[TOC]

# Introduction

In interactive Python, users can execute multiple commands. And to keep track of all the commands executed, Python stores a history of previously executed commands. However, there may be instances when the user wants to view the entire command history. 

In this article, we will discuss how you can execute commands to view the complete command history in interactive Python.

# Using the ‘history’ command

One way to view the history of all commands is by using the ‘history’ command. By default, this command displays the last 10 commands executed. However, you can pass an integer argument to the ‘history’ command, specifying the number of commands that you want to display.

Open the interactive Python shell and execute the following commands to view the history of previously executed commands:

```sh
>>> history
```

This will display the last ten commands executed. However, if you want to view more than ten commands, execute the command:

```sh
>>> history <n>
```

Where ‘n’ is an integer, specifying the number of commands that you want to display.


# Using readline module to display command history

Another way to view the entire command history is by using the readline module. The readline module provides a set of functions that enable users to edit and interactively execute history of commands. 

Follow the below steps to activate the readline module:

1. Open the interactive Python shell
2. Execute the following command to activate the module
```python
>>> import readline
```
3. Once readline is activated, use the simple keyboard shortcut ‘Ctrl+R,’ to view the complete command history. Pressing this combination will prompt you with an incremental search interface, allowing you to search the entire command history.

# Using the ‘_i’ and ‘_ih’ variables

Python automatically creates two variables every time a command is executed in the interactive shell. These variables are ‘_i’ and ‘_ih.’ 

The ‘_i’ variable stores the last command executed in the interactive shell, while the ‘_ih’ variable stores a list of all commands executed in the interactive session.

To view the entire history of commands executed in the interactive shell, execute the following command:

```sh 
>>> _ih 
```

This will access the ‘_ih’ variable, displaying all the commands previously executed in the shell.

# Conclusion

In conclusion, Python provides different methods to view the complete history of commands executed in the interactive shell. You can use the ‘history’ command, the readline module, or access the ‘_i’ and ‘_ih’ variables created by Python when a command is executed in the interactive shell.
