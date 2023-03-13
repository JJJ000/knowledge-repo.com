---
title: How can I keep a script running in the background even after logging out of ssh?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-13 00:00:00
updated_at: 2023-03-13 00:00:00
tldr: Use the nohup command to run the script in the background and redirect the output to a file, followed by the command to disconnect the SSH session.
---

**Contents**

[TOC]

## Introduction 
Sometimes, when running a Python script on a remote server via SSH, we want to ensure that the script continues running even after logging out. This tutorial outlines how to run a script in the background, even after logging out of SSH in Python.

## Solution
There are several ways to run a script in the background after logging out of SSH, following are two possible solutions:

### Solution 1: Using nohup command
One way to run a Python script in the background is by using the `nohup` command before running the script. `nohup` will ignore the hangup signal generated when the user logs out, which will keep the script running in the background. 

Here’s an example:
```python
nohup python script.py &
```

The `&` symbol at the end of the command is used to run the command in the background.

### Solution 2: Using screen command
Another way to run a Python script in the background is by using the `screen` command. This will allow the user to detach a screen session and then later reattach the session to the script when they log back in again.

Here’s an example:
```python
screen -S session_name
```
This will create a new screen session with the name `session_name`.

```python
python script.py
```
This will run the given script inside the screen session.

To detach from the screen session and let the script continue running in the background, use the keyboard shortcut `Ctrl+A` followed by the letter `d`.
When you log back in later, you can reattach the screen session by running the command:

```python
screen -r session_name
```

## Conclusion
These are two different methods for running a Python script in the background, even after logging out of SSH. Both methods serve the same purpose, but the `screen` command offers more flexibility for the user to reattach the detached session. On the other hand, `nohup` is a simpler solution that allows users to run scripts in the background with minimal setup.
