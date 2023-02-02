---
title: Execute a Python script from within another Python script, providing it with command line arguments
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-02 00:00:00
updated_at: 2023-02-02 00:00:00
tldr: You can use the subprocess module to run a Python script from another Python script, passing in arguments.
---

**Contents**

[TOC]

**Section 1 - Importing the Script**

The first step is to import the script that you want to run in the current script. This can be done using the `import` statement. For example, if the script you want to run is named `my_script.py`, you would write `import my_script` at the top of the current script.

**Section 2 - Passing Arguments**

The next step is to pass arguments to the script you are running. This can be done by passing the arguments as parameters to the script. For example, if the script you are running takes two arguments, `arg1` and `arg2`, you would write `my_script.run(arg1, arg2)` in the current script.

**Section 3 - Executing the Script**

The final step is to execute the script. This can be done by calling the `run()` method of the imported script. For example, if the script you are running is named `my_script.py`, you would write `my_script.run()` in the current script.

**Section 4 - Return Value**

If the script you are running returns a value, you can capture it by assigning the return value to a variable. For example, if the script you are running returns an integer, you can capture the return value by writing `result = my_script.run()` in the current script. The variable `result` will now contain the return value of the script.
