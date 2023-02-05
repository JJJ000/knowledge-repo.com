---
title: Save the result of a subprocess.popen call in a string
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: The output of the subprocess.Popen call can be stored in a string by using the communicate() method.
---

**Contents**

[TOC]

# Section 1: Overview
The output of a `subprocess.Popen` call can be stored in a string in Python by using the `communicate()` method.

# Section 2: Syntax
The syntax for using `communicate()` to store `subprocess.Popen` output in a string is as follows:

```python
process = subprocess.Popen(command, stdout=subprocess.PIPE)
output, error = process.communicate()
```

# Section 3: Explanation
The `subprocess.Popen` call is used to execute a command and the `communicate()` method is used to capture the output of the command. The `communicate()` method returns a `tuple` containing the output of the command (`stdout`) and any errors (`stderr`). The output of the command can then be stored in a string by assigning the `stdout` element of the `tuple` to a variable.

# Section 4: Example
The following example shows how to store `subprocess.Popen` output in a string:

```python
import subprocess

command = 'ls -l'
process = subprocess.Popen(command, stdout=subprocess.PIPE)
output, error = process.communicate()

output_string = output.decode('utf-8')
print(output_string)
```

The output of this code would be a string containing the output of the `ls -l` command.
