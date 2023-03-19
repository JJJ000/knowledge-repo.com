---
title: Executing Python code within vim
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-13 00:00:00
updated_at: 2023-03-13 00:00:00
tldr: Install the Vim plugin `python-mode` and use the command `Python` followed by the name of the Python script to run Python code in Vim.
---

**Contents**

[TOC]

There are multiple ways to run Python code in Vim. Here are three options:

## Option 1: Use Vim's built-in terminal
Vim has a built-in terminal that allows you to run commands and programs within Vim. To open the terminal, you can use the `:terminal` command. Once in the terminal, you can type `python` to start the Python interpreter and run your code.

1. Open your Python file in Vim:
```
$ vim myfile.py
```
2. Open the terminal:
```
:terminal
```
3. Start the Python interpreter:
```
python
```
4. Run your code:
```python
>>> print("Hello, world!")
Hello, world!
```

## Option 2: Use a Vim plugin
There are Vim plugins such as `vim-slime` and `vim-python-pep8-indent` that allow you to send your Python code from Vim to a separate terminal or Python interpreter. These plugins require additional installation and configuration, but can make the workflow smoother in the long run.

## Option 3: Use an external terminal
You can also run your Python code in an external terminal while editing in Vim. One common way to do this is to split the terminal and Vim windows horizontally or vertically, so that you can see both at the same time. Then, you can save your Python file in Vim and switch to the terminal to run it.

1. Open your Python file in Vim:
```
$ vim myfile.py
```
2. Split the terminal and Vim windows:
```
:sp
```
3. Save the Python file in Vim:
```
:w
```
4. Switch to the terminal:
```
<C-w><direction>
```
5. Run the Python file:
```
$ python myfile.py
```
