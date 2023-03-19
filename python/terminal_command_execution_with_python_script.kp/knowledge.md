---
title: Python scripts are capable of executing commands through the terminal
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-13 00:00:00
updated_at: 2023-03-13 00:00:00
tldr: Yes, a Python script can execute commands in the terminal by using the subprocess module.
---

**Contents**

[TOC]

## Introduction
Python is a versatile programming language that can be used for a variety of tasks, including executing commands in a terminal. In this article, we will explore how to execute commands in a terminal using a Python script. 

## Using the os module
The easiest way to execute terminal commands using a Python script is by using the `os` module. The `os` module provides a way to interact with the operating system, including executing terminal commands. To use the `os` module, you will first need to import it:

```python
import os
```

Once you have imported the `os` module, you can use the `os.system()` function to execute terminal commands. 

```python
os.system("ls")
```

The above command will execute the `ls` command in the terminal. You can replace `ls` with any other command that you would like to execute. 

## Using subprocess module
Another way to execute terminal commands using a Python script is by using the `subprocess` module. The `subprocess` module provides more flexibility than the `os` module when executing terminal commands. It allows you to execute commands with more options, such as setting environment variables or setting the working directory. 

To use the `subprocess` module, you will first need to import it:

```python
import subprocess
```

Once you have imported the `subprocess` module, you can use the `subprocess.run()` function to execute terminal commands. 

```python
subprocess.run(["ls", "-l"])
```

The above command will execute the `ls -l` command in the terminal. You can replace `ls -l` with any other command that you would like to execute. 

## Using Shell=True
Both the `os.system()` and `subprocess.run()` functions can take a parameter `shell=True`. If you set `shell=True` in either function, you can execute terminal commands with all of the shell's capabilities. 

```python
os.system("echo $HOME")
```

The above command will execute the `echo $HOME` command in the terminal and print the value of the `HOME` environment variable. 

However, it is important to note that setting `shell=True` can be a security risk. If you are executing commands with user input, it is recommended to use the `subprocess` module with individual arguments instead of `shell=True`. 

## Conclusion
Using a Python script to execute commands in a terminal can be very useful in automating tasks. The `os` and `subprocess` modules provide different options for executing commands and choosing the one that fits your needs best is important. However, when setting `shell=True`, it is recommended to be mindful of possible security risks.
